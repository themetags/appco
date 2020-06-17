Go to the `scripts.js` file and check the following code:

~~~js
// Subscription
  if($("#getQuoteFrm").length) {
    $("#getQuoteFrm").validator().on("submit", function (event) {
        if (event.isDefaultPrevented()) {
          // handle the invalid form...
            submitMSG(false);
        } else {
          // everything looks good!
            event.preventDefault();
            submitGetQuoteForm();
        }
    });
  }

  function submitGetQuoteForm(){
    // Initiate Variables With Form Content
    var name = $('#getQuoteFrm input[name="name"]').val();
    var email = $('#getQuoteFrm input[name="email"]').val();
    var subject = $('#getQuoteFrm input[name="subject"]').val();
    var message = $('#getQuoteFrm textarea[name="message"]').val();
    
    if (!$('#getQuoteFrm #exampleCheck1').is(":checked")) {
        submitMSG(false, '.sign-up-form-wrap');
        return;
    }

    $.ajax({
        type: "POST",
        url: "libs/quote-form-process.php",
        data: "name=" + name + "&email=" + email + "&subject=" + subject + "&message=" + message,
        success : function(text){
            if (text == "success"){
                quoteFormSuccess();
            } else {
                submitMSG(false, '.sign-up-form-wrap');
            }
        }
    });
  }

  function quoteFormSuccess(){
    $("#getQuoteFrm")[0].reset();
    submitMSG(true, '.sign-up-form-wrap');
  }

~~~

PHP file: libs/quote-form-process.php

Change the email address "hellothemetags@gmail.com" with your email address. Please make sure that you have given permission to send an email from your server.


~~~php
// change email with your email
$EmailTo = "hellothemetags@gmail.com";
$Subject = "AppCo:: New Message Received form get quote";

// prepare email body text
$Body = "";
$Body .= "Name: ";
$Body .= $name;
$Body .= "\n";
$Body .= "Email: ";
$Body .= $email;
$Body .= "\n";
$Body .= "Subject: ";
$Body .= $subject;
$Body .= "\n";
$Body .= "Message: ";
$Body .= $message;
$Body .= "\n";

// send email
$success = mail($EmailTo, $Subject, $Body, "From:".$email);

~~~


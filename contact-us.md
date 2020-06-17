### Forms
We have used 2 types of form in our template. The contact us form and Get a quote form. Both forms are done by the Ajax call and used PHP as a backend language. Here is the Javascript code and PHP code.

Go to the `scripts.js` file and check the following code:
~~~js
// contact form
    if($("#contactForm").length) {
        $("#contactForm").validator().on("submit", function (event) {
            if (event.isDefaultPrevented()) {
            // handle the invalid form...
                submitMSG(false, '.contact-us');
            } else {
            // everything looks good!
                event.preventDefault();
                submitContactForm();
            }
        });
    }


    function submitContactForm(){
        // Initiate Variables With Form Content
        var name    = $("#contactForm #name").val();
        var email   = $("#contactForm #email").val();
        var phone   = $("#contactForm #phone").val();
        var company = $("#contactForm #company").val();
        var message = $("#contactForm #message").val();

        $.ajax({
            type: "POST",
            url: "libs/contact-form-process.php",
            data: "name=" + name + "&email=" + email + "&phone=" + phone + "&company=" + company + "&message=" + message,
            success : function(text){
                if (text == "success"){
                    formSuccess();
                } else {
                    submitMSG(false, '.contact-us');
                }
            }
        });
    }

    function formSuccess(){
        $("#contactForm")[0].reset();
        submitMSG(true, '.contact-us');
    }

    function submitMSG(valid, parentSelector){
        if(valid){
            $(parentSelector + " .message-box").removeClass('d-none').addClass('d-block ');
            $(parentSelector + " .message-box div").removeClass('alert-danger').addClass('alert-success').text('Form submitted successfully');
        } else {
            $(parentSelector + " .message-box").removeClass('d-none').addClass('d-block ');
            $(parentSelector + " .message-box div").removeClass('alert-success').addClass('alert-danger').text('Found error in the form. Please check again.');
        }
    }

~~~


PHP file: libs/contact-form-process.php

Change the email address "hellothemetags@gmail.com" with your email address. Please make sure that you have given permission to send an email from your server.


~~~php
...

// change email with your email
$EmailTo = "hellothemetags@gmail.com";
$Subject = "AppCo:: New Message Received form contact";

// prepare email body text
$Body = "";
$Body .= "Name: ";
$Body .= $name;
$Body .= "\n";
$Body .= "Email: ";
$Body .= $email;
$Body .= "\n";
$Body .= "Phone: ";
$Body .= $phone;
$Body .= "\n";
$Body .= "Company: ";
$Body .= $company;
$Body .= "\n";
$Body .= "Message: ";
$Body .= $message;
$Body .= "\n";

// send email
$success = mail($EmailTo, $Subject, $Body, "From:".$email);

...
~~~



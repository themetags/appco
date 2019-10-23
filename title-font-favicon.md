### Changing title, fonts, favicon

You can update `title`, `favicon` `font` and also OG info with SEO meta description.


#### Title
In this head section you can find the `title` tag. Just replace the text on `title` tag.

```html
<!--title-->
<title>AppCo App Landing Page Template</title>
```

#### favicon
If you replace the `favicon.png` image or icon on `img` folder then favicon will automatically update. 
```html
<!--favicon icon-->
<link rel="icon" href="img/favicon.png" type="image/png" sizes="16x16">
```

#### fonts
Aptonic uses 2 fonts: Montserrat & Open+Sans from the [Google Fonts Library](https://fonts.google.com/). You can change the fonts file in below link on `head` section. 
If you want to use self hosted fonts other than Google fonts then here is an example of [self hosted fonts](https://css-tricks.com/snippets/css/using-font-face/). In this case you need to remove below link and change font names in `/scss/base/variable.scss` file as per your fonts used. 
Also you can change font-weights that you have used. Just change the variable value.
```html
<!--google fonts-->
<link href="https://fonts.googleapis.com/css?family=Comfortaa:500,600,700%7COpen+Sans&display=swap" rel="stylesheet">
```

We have used two fonts Sans and Comfortaa. For body we use Open Sans and all type of heading we used Comfortaa font.
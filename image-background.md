### How to change image and background image

**AppCo** download package does not contain images which are there in our online demo. We are using placeholder images instead of real images. You will see the image code as mentioned below. You can replace placeholder image url with your image url like `img/your-image.jpg` or `img/your-image.svg` or `img/your-image.png`

*We only included SVG images it's MIT license Open-source illustrations for every project you can use it.

#### for image
```html
<img src="your image path" alt="image alt text" class="img-fluid">
```

#### for background image
When you use background image then you should follow bellow structure `.background-img` need to call on parent `div`. 

```html
<section class="hero-section pt-100 background-img" style="background: url('img/hero-bg-2.jpg')no-repeat center center / cover">
    <div class="container">
        <div class="row">
            <!--SECTION CONTENTS-->
        </div>
    </div>
</section>
```




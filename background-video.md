### Background Video section

We have background video hero section please check demo 5 or `index-5.html`

#### How to use your video on this section
```html
<!--hero section start-->
<section class="hero-section background-img" style="background: url('img/hero-bg-2.jpg')no-repeat center center / cover">
    <div class="video-section-wrap">
        <div class="background-video-overly ptb-100">
            <div class="player" data-property="{videoURL:'https://www.youtube.com/watch?v=LV3cjaA7NtE',containment:'.video-section-wrap', quality:'highres', autoPlay:true, showControls: false, startAt:15, mute:true, opacity: 1}"></div>
            <div class="container">
                <div class="row align-items-center justify-content-center">
                    <div class="col-md-8 col-lg-7">
                        <div class="hero-content-left text-white text-center mt-5 ptb-100">
                           <!--HERO CONTENT-->
                        </div>
                    </div>
                </div>
                <!--clients logo start-->
                <div class="row justify-content-between">
                    <div class="col-md-12">
                        <div class="client-section-wrap d-flex flex-row align-items-center">
                            <p class="lead mr-5 mb-0 text-white">Trusted by companies like:</p>
                            <ul class="list-inline justify-content-between">
                                <!--CLIENT LOGOS IMAGES LIST-->
                            </ul>
                        </div>
                    </div>
                </div>
                <!--clients logo end-->
            </div>
        </div>
    </div>
</section>
<!--hero section end-->
```

This is background video hero section. In this section you can find bellow `div`. In this div you can see a youtube video link end of the link you can see your video ID like this `gOqlwlQjVis` you just replace this id. Another attribute is `startAt:0` it's mean this video start from 0.

```html
<div class="player" data-property="{videoURL:'https://www.youtube.com/watch?v=LV3cjaA7NtE',containment:'.video-section-wrap', quality:'highres', autoPlay:true, showControls: false, startAt:0, mute:true, opacity: 1}"></div>
```

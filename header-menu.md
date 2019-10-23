### Header Menu Item
You can find the menu inside the `nav` tag on header section. In this menu items you can change the menu text like - **Home**, **Features**, **Pricing** ...etc.

```html
<div class="collapse navbar-collapse main-menu" id="navbarSupportedContent">
    <ul class="navbar-nav ml-auto">
        <li class="nav-item active">
            <a class="nav-link page-scroll" href="#">Home</a>
        </li>
        <li class="nav-item">
            <a class="nav-link page-scroll" href="#about">About</a>
        </li>
        <li class="nav-item">
            <a class="nav-link page-scroll" href="#services">Service</a>
        </li>
        <li class="nav-item">
            <a class="nav-link page-scroll" href="#pricing">Pricing</a>
        </li>
        <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
               data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                Pages
            </a>
            <div class="dropdown-menu submenu" aria-labelledby="navbarDropdown">
                <a class="dropdown-item" href="about-us.html">About Us</a>
                <a class="dropdown-item" href="services.html">Our Services</a>
                <a class="dropdown-item" href="pricing.html">Our Pricing</a>
                <a class="dropdown-item" href="contact-us.html">Contact Us</a>
            </div>
        </li>
        <li class="nav-item">
            <a class="nav-link page-scroll" href="#contact">Contact</a>
        </li>

    </ul>
</div>
```
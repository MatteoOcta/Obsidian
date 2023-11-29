

```html
<div class="social-links all-links">
  <div class="social-link instagram">
    <p>
      <a href="https://www.instagram.com/my_cookies_fr/" target="blank" rel="noopener">
      	<i class="fa-brands fa-instagram"></i>
        <span>Instagram</span>
      </a>
    </p>
  </div>
  <div class="social-link facebook">
    <p>
      <a href="https://www.facebook.com/mycookiesfr" target="blank" rel="noopener">
    		<i class="fa-brands fa-facebook-f"></i>
    		<span>Facebook</span>
      </a>
    </p>
  </div>

    <div class="social-link tel">
    <p>
      <a href="tel:+33650010742" target="blank" rel="noopener">
    		<i class="fa-solid fa-phone"></i>
    		<span>Téléphone</span>
      </a>
    </p>
  </div>
</div>

```

CSS 
```css
#social-links-all {
    position: fixed!important;
    top: 40vh!important;
    right: 0;
    background: transparent!important
}

#social-links-all .social-links.all-links {
    display: flex;
    flex-direction: column;
    row-gap: 5px
}

#social-links-all .social-link {
    padding: 7.5px 5px 7.5px 10px;
    border-top-left-radius: 2.5px;
    border-bottom-left-radius: 15px;
    transform: translateX(92px);
    transition: all ease 0.4s
}

body.tax-product_cat #social-links-all .social-link {
    transform: translateX(70%)!important
}

body.tax-product_cat #social-links-all .social-link:hover {
    transform: translateX(0)!important
}

#social-links-all .social-link:hover {
    transform: translateX(0)!important
}

#social-links-all .social-link p a {
    display: flex;
    align-items: center
}

#social-links-all .social-link.instagram {
    background: #ce3565
}

#social-links-all .social-link.facebook {
    background: #1771e6
}

#social-links-all .social-link.tel {
    background: #00FF00
}

#social-links-all .social-link i {
    font-size: 1.5rem;
    padding-right: 15px;
    color: #fff
}

#social-links-all .social-link span {
    color: #fff;
    font-size: 1rem;
    line-height: 1rem
}
```
## Menu Flex
```css
#header ul#icemegamenu {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-evenly;
}
```

## Menu Top Flex

```css
#top .row{
  display: flex;
  flex-wrap: wrap;
  align-items: center;
}
```

## Title Slider 

```css
/* slider */
#swiper-slider_208 .flex-title
{
  display: flex;
  justify-content: center;
  align-items: center;
  column-gap: 2.5%;
  font-family: var(--title-font);
  color: var(--primary-color);
}

#swiper-slider_208 .flex-title .big-title
{
  position: relative;
  font-size: 4.0625rem;
  line-height: 4.0625rem;
  font-weight: 700;
}

#swiper-slider_208 .flex-title .big-title::after
{
  position: absolute;
  content: "";
  width: 100%;
  left: 0;
  bottom: -15px;
  border-bottom: 5px solid var(--primary-color);
}

#swiper-slider_208 .flex-title .thin-title
{
  position: relative;
  font-size: 2.6875rem;
  line-height: 2.6875rem;
  font-weight: 400;
  font-style: italic;
}

#swiper-slider_208 .flex-title .bold-title
{
  position: relative;
  font-size: 2.5rem;
  line-height: 2.5rem;
  font-weight: 700;
  text-transform: uppercase;
}

#swiper-slider_208 .flex-title p
{
  max-width: fit-content;
  padding-bottom: 0;
}
```

### HTML
```html
<div class="flex-title">
<p class="big-title">Camille Rigaud</p>
<div class="two-row-title">
<p class="thin-title">Bien-être</p><p class="bold-title">psychologie</p>
</div>
</div>
<a class="btn btn-info readmore" href="/contact-prise-de-rendez-vous" target="_self"><span>Me contacter</span></a>

```
## Bloc vidéo 

```css
#maintop{
  background: url(../images/bg-1.png) no-repeat;
  min-height: 613px;
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  justify-content: center;
  color:white;
}
#maintop header h3{
  color:white;
  text-align: center;
  max-width: 404px;
  margin:0 auto;
  margin-bottom: 30px;
}
#maintop .mod-custom{
  max-width: 1060px;
  text-align: center;
  margin:0 auto;
}
```

## Testimonial flex
```css
.mod-newsflash-adv.testimonials .item_content{
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  justify-content: center;
}

.mod-newsflash-adv.testimonials .item_content figure{
  flex:20%;
  margin-right: 0;
}
.mod-newsflash-adv.testimonials .item_content div{
  flex:80%;
}
.mod-newsflash-adv.testimonials .item .item_content .item_img:after, .mod-newsflash-adv.testimonials .item .item_content .item_img:before{
  left:90% !important;
}
```

## 3 Items Tabs
```css
#feature .nav-tabs {
  display: flex;
  flex-wrap: wrap;
}
#feature .nav-tabs li{
  flex: 33%;
}
```


![[Pasted image 20230216132516.png]]

## Tabs Flex 
```css
.tab-content .mod-article-single .item__module{
  display: flex;
  align-items: center;
  flex-wrap: wrap;
}
.tab-content .mod-article-single .item__module div.icons{
  display: none;
}
.tab-content .mod-article-single .item__module figure{
  flex:20%;
  max-width: 29%;
}
.tab-content .mod-article-single .item__module > div.item_content {
  flex:80%;
  max-width: 65%;
}
ul.nav-tabs a{
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  justify-content: space-between;
  min-height: 100%;
}
ul.nav-tabs{
  display: flex;
  align-items: stretch;
  flex-wrap: wrap;
}
```

![[Pasted image 20230216132614.png]]
## Bloc 3 

```css
.mod-newsflash-adv__center.cols-3 .row{
  display: flex;
  flex-wrap: wrap;
   flex-direction: row;
  justify-content: space-between;
  min-height: 100%;
}
.mod-newsflash-adv__center.cols-3 .row .item {
  display: flex;
  align-items: stretch;
  flex-wrap: wrap;
}

```
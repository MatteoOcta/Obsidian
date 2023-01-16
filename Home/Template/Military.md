## Menu Flex
```css
#header ul#icemegamenu {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-evenly;
}
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
```
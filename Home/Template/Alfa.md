## Custom ico top
```css
[class*="customico-top"]{
  font-size:0;
  float: left;
  line-height: 0;
}

[class*="customico-top"]:before{
  line-height: 40px;
  margin: 0 14px 0 2px;
  font-size:1rem;
}

.customico-top_ico1:before{
  content:url("../images/ico/ico1.png");
}

.customico-top_ico2:before{
  content:url("../images/ico/ico2.png");
}
```

## Menu flex
```css
.navbar-mainmenu ul.navbar-nav {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-evenly;
}
```

## Bloc 4 images / counter + texte FLEX

```css
.mod-newsflash-adv__center.about.cols-2 .row,.body__home .position-3 .row{

  display: flex;

  flex-wrap: wrap;

  align-items: center;

}

.mod-newsflash-adv__center.about.cols-2 .row article, .body__home .position-3 .row div{

  flex: 50%;

}
```


## Mini border sous title

```css
h3{
padding-bottom:6%;
}

h3:after{
  content:" ";
  border-top: 2px solid var(--octa-color-secondary);
  width: 100%;
  max-width: 25px;
  position: relative;
  display: block;
  top:7px;
}
```

## Menus Top

```css
#t3-header div.row {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
}
```
## Media menus top
```css
@media (max-width: 970px) {
  #t3-header div.row .col-sm-5{
    flex:100%;
  }
  ul.top-menu > li{
    padding-left: 44px;
  }
  ul.top-menu{
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    gap:3px;
  }
  ul.top-menu li{
    flex:20%;
  }
  #t3-header .row .col-sm-12 ul.navbar-nav{
    gap:1rem;
  }
}

@media (max-width: 770px) {
  #t3-header .row .col-sm-12 ul.navbar-nav li{
    flex:100%;
 }
  #t3-header div.row .col-sm-2 {
  width: 100%;
 }
 .link{
  margin:  0 auto;
 }
}
@media (max-width: 545px) {
  ul.top-menu li{
    flex:100%;
  }
  ul.top-menu{
    text-align: center;
  }
}
```

## Bloc 4 item Services -> 2 centrer 

```css
.position-2 .mod-newsflash-adv__services.cols-2 .row{
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
.position-2 .mod-newsflash-adv__services.cols-2 .row .col-sm-6{
width:auto;
justify-content: center;
}
```

## Btn top 

```css
.menu.link a.link{
  border:var(--octa-color-primary) solid 2px;
  background: white;
  color:var(--octa-color-primary);
  border-radius:99px;
  text-transform: none;
}

.menu.link a.link:hover{
  border: 2px transparent solid;
  color:white;
  background:var(--octa-color-primary);
}

```
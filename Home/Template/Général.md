## Import font 

```css
@font-face {
  font-family: "Photograph-Signature";
  src: url("../fonts/Photograph-Signature.ttf") format("truetype");
}
```


## Btn

```css
 a.btn{
  border: 2px transparent solid;
  color:white;
  background:var(--octa-color-primary);
  border-radius:99px;
  text-transform: none;
}


a.btn:hover{
  border:var(--octa-color-primary) solid 2px;
  background: white;
  color:var(--octa-color-primary);
}
```
![[Pasted image 20221221095950.png]]
## Btn reverse

```css
a.btn{
  border:var(--octa-color-primary) solid 2px;
  background: white;
  color:var(--octa-color-primary);
  border-radius:99px;
  text-transform: none;
}

a.btn:hover{
  border: 2px transparent solid;
  color:white;
  background:var(--octa-color-primary);
}
```
![[Pasted image 20221221095841.png]]

## News flash adv FLEX 
```css
.mod-newsflash-adv__blog .row{ /** Row **/
  display: flex;
  align-items: stretch;
  flex-wrap: wrap;
}
.mod-newsflash-adv__blog article.col-sm-4 .item_content { /** Items **/
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  justify-content: space-between;
  min-height: 100%;
}
```

## Flex 3 item + icones footer 

![[Pasted image 20230116131014.png]]

```css 
#copyright .mod-custom .flexThird > div{
  display: flex;
  flex-direction: column;
  align-items: center;
  flex-wrap: wrap;
}
#copyright .mod-custom .flexThird > div p{
  text-align: center;
  display: flex;
  align-items: center;
}
[class*="custom-ico"]:before{
  padding: 13px;
}
.custom-ico-1:before {
  content:url("../images/ico/ico-1.png")
}
.custom-ico-2:before {
  content:url("../images/ico/ico-2.png")
}
.custom-ico-3:before {
  content:url("../images/ico/ico-3.png")
}
```

```html
<div class="flexThird">
    <div><h3>Nous situer</h3> <p class="custom-ico-1">#</div>
    <div><h3>Nous joindre</h3> <p class="custom-ico-2"><a href="#"></a></p>#</div>
    <div><h3>Nous contacter</h3> <p class="custom-ico-3"><a href="#">#</a></p></div>
</div>
```

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

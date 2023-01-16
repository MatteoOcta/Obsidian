## A PAS 

```html 
<p class="center"> <i> Contenu a venir </i> </p>
```


## Cadre_animée

```css

.encart
{
  position: relative;
  text-align: center;
  padding: 50px 100px;
  margin: 50px 0;
  font-size: 1rem;
}

.encart::before
{
  position: absolute;
  content: "";
  left: 0;
  bottom: 0;
  width: 17.5%;
  height: 40%;
  border-bottom: 3px solid #B52F29;
  border-left: 3px solid #B52F29;
  transition: all ease 0.4s;
}

.encart::after
{
  position: absolute;
  content: "";
  right: 0;
  top: 0;
  width: 17.5%;
  height: 40%;
  border-top: 3px solid #B52F29;
  border-right: 3px solid #B52F29;
  transition: all ease 0.4s;
}

  

.encart:hover::before,
.encart:active::before,
.encart:focus::before,
.encart:hover::after,
.encart:active::after,
.encart:focus::after
{
  width: calc(100% - 3px); /* On soustrait l'épaisseur de la bordure*/
  height: calc(100% - 3px);
}
```

  

## Youtube 
```html
<div class="youtube_player" videoID="video_id" width="750px" height="500px" theme="light" rel="1" controls="1" showinfo="1" autoplay="0" mute="0"></div>
```

### CSS Youtube

```css
.youtube_player iframe{
  width:100% !important;
 }
```

## Marcaron

 ```css
.macaron {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  row-gap: 10px;
  text-align: center;
  padding: 30px;
  background: #214477;
  color: #fff;
  height: 5rem;
  width: 60px;
  border: 7px solid white;
  border-radius: 50%;
  margin: 0 auto;
}
```


## Carte animé

```css
.card{
  width: 40%;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 30px;
  box-shadow: 0 0 15px #bbbbbb;
  border-radius: 10px;
  transition: all ease 0.4s;
  text-align: center;
  border: 1px solid #ebebeb;
}

.card h3{
  position: relative;
  max-width: fit-content;
  margin: 0 auto;
  padding: 0 15px 15px;
}

.card h3::before,
.card h3::after{
  position: absolute;
  content: "";
  top: calc(50% - 7.5px);
  width: 30px;
  border-top: 1px solid var(--primary-color);
} 

.card h3::before{
  left: -30px;
}

.card h3::after{
  right: -30px;
}

.card:hover{
  transform: scale(1.1);
  box-shadow: 0 0 15px #858585;
}
```

## Bloc un sur deux de chaque coté

```css
.content_lr > div:nth-child(odd){
  margin-left: 20px;
  border-left: var(--octa-color-primary) 4px solid;
  padding-left: 20px;
  text-align: left;
  margin-bottom: 10px;
}

.content_lr > div:nth-child(even){
  margin-right: 20px;
  border-right: var(--octa-color-primary) 4px solid;
  padding-right: 20px;
  text-align: right;
  margin-bottom: 10px;
}
```

### HTML 
```html
<div class="content_lr">
<div> 
<h2> </h2>
<p> </p>
</div>
<div>
<h2> </h2>
<p> </p>
</div>
</div>
```

<h1>Gallery Sass</h1>
<div align="center">
  <img src="./assets/img/galleryPrint.svg">
</div>

<h2 align="center"><a href="https://wesley-wilson.github.io/gallery-sass/" target="_blank">project</a></h2>

<br>

## 📕About

Learning application in **Sass** technology, where you can see the use of variables and functions for better use of styling in the site, giving a greater margin of organization and transparency

<br>

## Variables
**Variables allow you to reduce repetition and use them in functions as you can see in this project**

to create a variable in sass you assign a value to a name that starts with $, and then you can refer to that name instead of the value itself.

```bash
$secondary-color: #20c997
```
To use the variable in the sass style sheet just call the name of the file, in this case the name created was **_variabels.sass** then **.$** and the name of the variable assigned to the property
example :
```bash
color: variables.$secondary-color
```

<br>

## @Mixins and @Include
The name of a mixin can be any Sass identifier and can contain any non-higher-level instruction. To learn more about higher education click 
[here](https://sass-lang.com/documentation/syntax/structure#top-level-statements)

```bash
@mixin flex-center
  display: flex
  justify-content: center
  align-items: center
```
Mixins are included in the current context using @includeregra at, which is written @include <name> or @include <name>(<arguments...>), with the name of the mixin included.
```
@include mixins.flex-center
```
<br>

## Parent Selector 
You nestedly call the children of the container that fall under the same class name. Using **&** you get a greater increase in productivity and agility using this way. 
example:
### **Sass**
```bash
.header
  display: flex
  justify-content: space-between
  @include mixins.container

  @include mixins.mobile
    padding: 1.1rem

  &-brand // .header-brand
    color: variables.$primary-color
    font-size: 3rem
  
  &-navbar
    ul
      height: 100%
      @include mixins.flex-center
```
### **Css**
```bash
.header {
  display: flex;
  justify-content: space-between;
  max-width: 1170px;
  padding: 1.5rem 0;
  margin: 0 auto;
}
@media (max-width: 425px) {
  .header {
    padding: 1.1rem;
  }
}
.header-brand {
  color: #fff;
  font-size: 3rem;
}
.header-navbar ul {
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
```
## Nesting
sass nesting is very simplified without having to call the previous name of the parent, just indicate and enjoy the application
### **Sass**
```bash
body
  background: variables.$bg-color
  color: variables.$text-color 

  a
    color: variables.$text-color 
    text-decoration: none
    transition: .4s
  
  ul
    list-style: none
```
### **Css**
```bash
body {
  background: #000;
  color: #777;
}
body a {
  color: #777;
  text-decoration: none;
  transition: 0.4s;
}
body ul {
  list-style: none;
}
```
## @content
Works as a **slot** to add specific codes to each element you want to apply
```bash
@mixin mobile
  @media(max-width: 425px)
    @content
```
## connection
To connect sass to css type in your project's built-in terminal **sass --watch** so that sass becomes a mirror of css, and everything that is changed in sass is changed in css.
Just remember the directory path and everything will be fine.
```bash
 sass --watch assets/sass/style.sass:assets/css/style.css
```



 ## 🔨 Tools
 - [HTML](https://developer.mozilla.org/pt-BR/docs/Web/HTML)
 - [CSS](https://developer.mozilla.org/pt-BR/docs/Web/CSS)
- [SASS](https://sass-lang.com/guide)

<br>

## Matheus Battisti
Professor Fernando Leonid's video channel to complement the remote classes.
- [Video](https://www.youtube.com/watch?v=Wo5t3uUV8n4&list=LL&index=30&t=1510s
)

## Thanks 
Picking up solid knowledge in the javascript language with the help of [Gustavo Guanabara](https://www.cursoemvideo.com/curso/javascript/), [Matheus Battisti](https://www.youtube.com/@MatheusBattisti) and other teachers who leave their free content on the internet.




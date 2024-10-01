# [![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=26&pause=1000&color=30F714&background=703BE2BE&center=true&vCenter=true&width=435&lines=Dia+10+clase;Introduccion+CSS;Sesion+01+CSS;IDAT+frontEnd)](https://git.io/typing-svg)

 >- **Hoja de estilos en cascada**
 >
 >CSS es uno de los lenguajes base de la Open Web y posee una especificación estandarizada por parte del W3C.
 >
 >Anteriormente, el desarrollo de varias partes de las especificaciones de CSS era realizado de manera sincrónica, lo que permitía el versionado de las recomendaciones.
 >
 >Probablemente habrás escuchado acerca de CSS1, CSS2.1, CSS3.
 >Sin embargo, CSS4 nunca se ha lanzado como una versión oficial.

## VINCULACION HTML - CSS

1. Hoja de estilo externa usando etiqueta "link"

```html
<link rel="stylesheet" href="./styles.css" />
```

2. Usando la etiqueta "style"

```css
<style>
  h1 {
    color: red;
  }
</style>
```

3. De manera inline en el elemento con el atributo "style"

```html
<h1 style="color: red">CSS</h1>
```

## SINTAXIS

- **Como se puede establecer codigo CSS**

```css
h1 {
  color: red;
}
```

- **h1** : _Selector_
- **color** : _Propiedad_
- **red** : _Valor_

## CONCEPTOS IMPORTANTES CSS

- **4 Conceptos importantes de CSS**

### _SELECTORES_

- _Indica a que elemento o elementos, se aplicara estilos._

```css
/* SELECTOR DE ETIQUETA */
h1 {
  color: red;
}
 
/* SELECTOR DE DESCENDENCIA */
nav ul li a {
  color: red;
}
```

### _HERENCIA_

- _Elementos ancestros heredan algunas propiedades a sus descendientes._

```html
<p>Hola mundo <a href="#">Esto es un enlace</a></p>
```

```css
p {
  color: peru;
}
 
a {
  color: inherit;
}
```

### _CASCADA_

- _Significa que los estilos que llegan en ultimo lugar , sobreescriben a los de antes._
- _La especificidad vence a la cascada_

```css
h1 {
  color: red;
}
 
h1 {
  color: blue;
}
```

### _ESPECIFICIDAD_

- _Es un valor numerico que adquieren los selectores y se aplica cuando hay conflictos_

```html
<!-- Selector de Etiqueta (1) -->
 
<!-- Selector de Clase (10) -->
 
<!-- Selector de ID (100) -->
 
<!-- INLINE (1000) -->
 
<!-- IMPORTANT (infinito) -->
```

```css
  (infinito) */
/* Selector de Etiqueta (004) */
nav ul li a {
  color: red;
}

/* Selector de Etiqueta (001) */
a {
  color: blue;
}

/* INLINE (1000) */
<h1 style="color: red;">CSS <span>Cascade Style Sheet</span></h1>

/* ESPECIFICIDAD: IMPORTANT (infinito) */
<!-- No es muy recomendable usarlo mucho , ya que puede  generar  conflictos  con   otros  estilos -->
.padre #hijo {
  color: red;
}

h1 {
  color: blue !important;
}

/* ESPECIFICIDAD: clase y ID = 110 */
.padre #hijo {
  color: red;
}
```

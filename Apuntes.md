# Apuntes de Clases HTML




## Roles

Si se quiere crear un rol que no está en la lista dejada abajo, se puede hacer mediante el uso de `div`

```html
    <div role="button">
        Haz click aquí
    <div>
```
Consultar los distintos roles en HTML -> https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles

## Listas
Existen las listas desordenadas, que se escriben con `<ul>`
```html
<ul>
    <li class="list-items"> Arauco 2023</li>
    <li class="list-items"> John Deere 2023</li>
    <li class="list-items"> Municipalidad 2022</li>
</ul>
```

<ul>
    <li class="list-items"> Arauco 2023</li>
    <li class="list-items"> John Deere 2023</li>
    <li class="list-items"> Municipalidad 2022</li>
</ul>
__________________________________________________________________________________________________________________________

Y las listas ordenadas `<ol>` estas se les puede cambiar el tipo, poner en reversa o cambiar de donde empiezan

<ol type="1" reversed start="10">
    <li class="list-items"> Arauco 2023</li>
    <li class="list-items"> John Deere 2023</li>
    <li class="list-items"> Municipalidad 2022</li>
</ol>

## Atributos booleanos
Los booleanos en HTML no se marcan con True o False, sino que siempre que se coloquen
es True, un ejemplo es el atributo "hidden" que oculta las imagenes

```html
<img 
headen
id="photo-image"
width="200"
height="250"
tittle= "Logo de Wall street silver"
alt ="Logo de Wall street silver" 
src="/images/prueba.jpg"
>
```

## Main 
A la hora de designar cuales serán los elementos dentro de main y cuales no se debe tener en cuenta lo siguiente, en este caso, el elemento main corresponde a la parte 
cambiante en cada noticia, Lo que es el titulo y lo que sigue de la noticia como tal,
pero la parte superior es común en las páginas, por lo que no entra en el main ni la parte superior, ni el footer

![Texto alternativo](/images/Ejemplo_main.png)

## Enlaces Internos y Externos
Todos los enlaces tanto internos como externos van en la sección de header, estos se escriben dentro de un `<nav>`

```html
        <nav>
            <a href="#Experiencia">Experiencia</a>
            <a href="#Proyectos">Proyectos</a>
            <!--Enlaces Internos y externos-->
            <a href="#https://twitch.tv/midudev" target="_blank"
            rel="noreferrer">twitch</a>

        </nav>
```

Para que funcione el enlace interno se debe luego referenciar con un id en algun titulo

```html
<h2 id="Proyectos"> Proyectos realizados "Presuntamente"</h2>
```
En el caso del enlace externo `target="_blank"` sirve para que se abra otra pestaña con el enlace, y `rel="noreferrer"` por temas de seguridad

También existen enlaces especiales para las formas de contacto
```html
<footer>
    Copyright 2023 - El Portfolio más bello del mundo

    <a href="mailto:fernando.parra@uc.cl">Enviame un correo</a>
    <a href="tel:+56923231">Llamar por telefono</a>
    <a href="whatsapp://send?text=Hola Mundo">Enviar mensaje</a>
</footer>
```

## Imagenes

Esta es una imagen tipica

```html
<img 
loading="lazy"
id="photo-image"
width="200"
height="250"
tittle= "Logo de Wall street silver"
alt ="Logo de Wall street silver" 
src="/images/prueba.jpg"
>
```
El `loading="lazi"` es para que no se carguen todas las imagenes si aun no se han visto, optimiza la pagina. Aunque no se deben usar en  imagenes del principio
Puedo hacer que la imagen se descargue cuando la pinchen, y esta forma es la misma para videos, archivos, etc...

```html
<a download href="/images/prueba.jpg">
    <img 
    id="photo-image"
    width="200"
    height="250"
    tittle= "Logo de Wall street silver"
    alt ="Logo de Wall street silver" 
    src="/images/prueba.jpg">
</a>
```
## Identificadores
Existen los identificadores unicos como el tipo `id`, el cual no se puede repetir en toda la pagina, y los identificadores para conjuntos de elementos como `class` 

```html
<ul>
    <li class="list-items"> Arauco 2023</li>
    <li class="list-items"> John Deere 2023</li>
    <li class="list-items"> Municipalidad 2022</li>
</ul>
```

```html
<h2 id="Proyectos"> Proyectos realizados "Presuntamente"</h2>
```

## Formularios

Codigo base para armar un formulario

<section>
    <h2>Formulario de Contacto</h2>
    <form method="post" action="">
        <fieldset>
            <legend>Información Personal</legend>
            <label for="name">Nombre:</label>
            <input type="text" id="name" name="name" placeholder="Fernando Parra">
        </fieldset>
    </form>
</section>


```html
<section>
    <h2>Formulario de Contacto</h2>
    <form method="post" action="">
        <fieldset>
            <legend>Información Personal</legend>
            <label for="name">Nombre:</label>
            <input type="text" id="name" name="name" placeholder="Fernando Parra" required>
        </fieldset>
    </form>
</section>
```
2 formas de hacer lo mismo
```html
            <label>Nombre:
            <input 
            type="text" 
            name="name" 
            placeholder="Fernando Parra"
            required>
            </label>
```


## Páginas de interes

Consultar los distintos roles en HTML -> https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles
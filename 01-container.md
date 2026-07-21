Para desarrollar Bootstrap desde cero, con un enfoque cien por ciento teórico, claro y paso a paso, vamos a desglosar los conceptos solicitados (los tipos de contenedores y el sistema de medidas) utilizando exclusivamente los códigos estrictamente necesarios para justificar la teoría, sin clases de diseño estético como bg-dark u otras distracciones visuales.
### 1. ¿Cómo se vincula Bootstrap a un proyecto? (Teoría base)
Bootstrap es un framework CSS. Esto significa que es un archivo externo lleno de estilos ya programados que se integra a nuestro documento HTML para aplicar diseños mediante clases predefinidas y lograr que la página sea responsiva automáticamente.
Para que el navegador entienda estas clases, debemos enlazar el archivo CSS de Bootstrap (vía CDN) dentro de la sección <head> de nuestro HTML:
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Curso Bootstrap</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
    </body>
</html>

```
### 2. Los Contenedores (container) - Teoría
Los contenedores son elementos estructurales obligatorios en Bootstrap. Su función principal es **centrar el contenido** en la pantalla y otorgar márgenes de seguridad laterales automáticos para que los textos o elementos no queden pegados a los bordes de la pantalla.
Existen principalmente dos tipos de contenedores estables:
 1. **.container (Contenedor Puro / Fijo):** Su ancho cambia de forma escalonada (puntos de quiebre o *breakpoints*) dependiendo de la resolución de la pantalla (celular, tablet, monitor). Deja márgenes automáticos a los lados.
 2. **.container-fluid (Contenedor Fluido):** Ocupa siempre el **100% del ancho** disponible de la pantalla de lado a lado, sin importar si estás en un dispositivo pequeño o en un monitor gigante.
#### Ejemplo 1: Uso exclusivo de un contenedor puro (.container)
Este código muestra cómo se estructura un archivo utilizando únicamente el contenedor fijo. La teoría justifica que el contenido interno se mantendrá centrado y con límites de ancho fijos según la pantalla.

[Link: Ejemplo codigo Container](https://hector-espacio.github.io/Bootstrap-guia/01-container/EjContainer.html)

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Ejemplo Container Puro</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

    <div class="container">
        <h1>Este es un título dentro de un .container puro</h1>
        <p>El contenido de este bloque se mantiene centrado y delimitado por márgenes automáticos en los laterales según el tamaño de la pantalla.</p>
    </div>

</body>
</html>

```
#### Ejemplo 2: Uso de otro tipo de contenedor (.container-fluid)
Este código muestra el contenedor fluido. La teoría justifica que este elemento ignorará los márgenes fijos laterales y se expandirá de extremo a extremo en todo el ancho del visor del navegador.
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Ejemplo Container Fluido</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

    <div class="container-fluid">
        <h1>Este es un título dentro de un .container-fluid</h1>
        <p>Este bloque ocupa el 100% del ancho de la pantalla de lado a lado, ideal para franjas o barras que requieran abarcar todo el espacio horizontal.</p>
    </div>

</body>
</html>

```
### 3. Las Medidas y Espaciados (Del 0 al 5) - Teoría
En Bootstrap, para gestionar los espacios (márgenes exteriores con la letra m y rellenos interiores con la letra p), no se utilizan píxeles fijos de forma directa en el código CSS tradicional, sino una **escala numérica del 0 al 5**.
Esta escala se basa internamente en múltiplos de una unidad base estándar (donde cada número representa un incremento proporcional):
 * **0**: Sin espacio (0px).
 * **1**: Espacio mínimo (4px).
 * **2**: Espacio pequeño (8px).
 * **3**: Espacio mediano o estándar (12px).
 * **4**: Espacio grande (16px).
 * **5**: Espacio máximo estándar (48px).
**Orientación de las letras clave:**
 * m = *margin* (margen exterior).
 * p = *padding* (relleno interior).
 * t = *top* (arriba).
 * b = *bottom* (abajo).
 * s = *start* (izquierda).
 * e = *end* (derecha).
 * x = horizontal (izquierda y derecha simultáneamente).
 * y = vertical (arriba y abajo simultáneamente).
#### Ejemplo 3: Aplicación de las medidas del 1 al 5
El siguiente ejemplo de código demuestra cómo aplicar estrictamente la teoría de las medidas utilizando un contenedor puro y diversas etiquetas de párrafo con diferentes niveles de espacio (mt-1 hasta mt-5), justificando matemáticamente y estructuralmente el distanciamiento superior de cada elemento sin usar clases estéticas ajenas:
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Ejemplo de Medidas Bootstrap</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

    <div class="container">
        <p>Texto base sin modificación de espacio superior.</p>

        <p class="mt-1">Este párrafo tiene la clase mt-1 (margen superior 1).</p>

        <p class="mt-2">Este párrafo tiene la clase mt-2 (margen superior 2).</p>

        <p class="mt-3">Este párrafo tiene la clase mt-3 (margen superior 3).</p>

        <p class="mt-4">Este párrafo tiene la clase mt-4 (margen superior 4).</p>

        <p class="mt-5">Este párrafo tiene la clase mt-5 (margen superior 5, separación amplia).</p>
    </div>

</body>
</html>

```

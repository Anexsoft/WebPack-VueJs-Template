# Webpack +VueJs Template by Anexsoft

> Este es un template para Webpack y VueJs que nos va a permitir registrar nuestros componentes de manera global e independiente.

La ventaja de este es que nos permite registrar componentes para un solo archivo cuando queremos cosas globales (global.main.js) y archivos independientes cuando nuestro componente solo debería existir para cierto módulo de nuestro sistema. Por ende, con este evitamos tener todo en un solo archivo y ganar performance hacia el Browser.

## Requisitos previos
Debemos tener instalado el client de Vue para que pueda compilar las extensiones .vue.

``` bash
npm install -g vue-cli
```

## Clonando el repositorio
``` bash
# Elijan la carpeta donde queremos clonar
cd my-project-path

# Corramos el comando para clonar
git clone https://github.com/Anexsoft/WebPack-VueJs-Template

# Actualizamos las dependencias
npm install
```

## Compilando nuestros componentes
Si ya tiene todo listo ahora debemos compilar nuestros componentes. Tenemos 2 entornos uno de DEV (para pruebas) el cual creará un servidor local para poder probar nuestros componentes y luego el BUILD que será el de producción creando un archivo .js que deberemos agregar a nuestro proyecto final.

``` bash
# Crea un servidor local para que puedas probar tus componentes
npm run dev

# Genera los javascripts
npm run build
```

## En tu archivo HTML
Luego de tener compilado los componentes deberás agregarlos a tu proyecto siendo el global.components.js el primero antes que los demás porque este contiene a VueJs. Asimismo, deberás ejecutar el siguiente código javascript para inicializar el registro de los componentes.

### Javascript Style
``` js
window.addEventListener('load', function() {
    new Vue({
        el: '#app',
        components: Components
    })
})
```

### jQuery Style
``` js
$(document).ready(function() {
    new Vue({
        el: '#app',
        components: Components
    })
})
```

## Anexsoft
En la siguiente publicación de Anexsoft podremos encontrar un videtutorial con un ejemplo práctico sobre el uso de este template.

Link:
[Publicación oficial de Anexsoft](http://anexsoft.com/p/176/plantilla-webpack-vuejs-para-nuestros-nuevos-proyectos)

## Créditos
Para realizar este template me base del oficial por parte de Vue, el mio digamos que es una personalización.

Fuente:
https://github.com/vuejs-templates/webpack-simple
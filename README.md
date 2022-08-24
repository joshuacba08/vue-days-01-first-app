# VueJS #Día 01

Bienvenidos a nuestro día 1 con VueJS. Para empezar, vamos a considerar los siguientes requerimientos:

- Node JS
- npm
- git

## Creación de un proyecto en VueJS

Podremos instalar y crear un nuevo proyecto en VueJS desde la página oficial: https://vuejs.org Entonces usaremos el siguiente comando:

```shell
npm init vue@latest
```

Al correr este comando vamos a crear un nuevo proyecto en VueJS, por lo que veremos en nuestra consola la siguiente interfaz:

```sh
✔ Project name: … <your-project-name>
✔ Add TypeScript? … No / Yes
✔ Add JSX Support? … No / Yes
✔ Add Vue Router for Single Page Application development? … No / Yes
✔ Add Pinia for state management? … No / Yes
✔ Add Vitest for Unit testing? … No / Yes
✔ Add Cypress for both Unit and End-to-End testing? … No / Yes
✔ Add ESLint for code quality? … No / Yes
✔ Add Prettier for code formatting? … No / Yes

Scaffolding project in ./<your-project-name>...
Done.
```

Si no estamos seguros de alguna configuración, basta con elegir **NO** y continuar con la siguiente configuración. Más adelante podremos incluir lo que nos haga falta a nuestro proyecto.

Veremos que se creará una carpeta con el nombre de nuestro proyecto en VueJS, por lo cual será necesario ingresar e iniciar nuestro proyecto mediante los siguientes comandos:

```shell
cd <your-project-name>
npm install
npm run dev
```

Aún no estamos en condiciones de realizar un build de nuestro proyecto, pero aún así dejo el comando para hacer el build de nuestra aplicación:

```shell
npm run build
```



## Usando la CLI de VueJS

Además de las configuraciones mencionadas anteriormente, podemos hacer uso del CLI de VueJS, un CLI significa "interfaz de línea de comandos", y es una herramienta sumamente importante a la hora de automatizar la creación y actualización de proyectos con un determinado framework. 

Podemos instalar nuestra CLI de VueJS desde su página oficial: https://cli.vuejs.org En todo caso, usaremos el siguiente comando:

```shell
npm install -g @vue/cli
```

[^CLI]: Command Line Interface

Una vez que hayamos instalado el CLI, podremos iniciar un nuevo proyecto en VueJS con el siguiente comando:

```shell
vue create 01-first-app
```

Lo que veremos a continuación es que el CLI nos proveerá de tres opciones para iniciar nuestro proyecto:

```shell
Vue CLI v5.0.8
? Please pick a preset:
  Default ([Vue 3] babel, eslint)
  Default ([Vue 2] babel, eslint)
> Manually select features
```

Las dos primeras son pre configuraciones para trabajar con Vue 2 o Vue 3, ambas son versiones de VueJS muy usadas. Mientras escribo este material, Vue 2 continúa siendo la versión más usada, sin embargo en un futuro no muy lejano primará Vue 3 en la mayoría de proyectos con este framework. 

Para esta instancia usaremos la opción 3 que es la de seleccionar las características de forma manual.

```shell
Vue CLI v5.0.8
? Please pick a preset: Manually select features
? Check the features needed for your project: (Press <space> to select, <a> to toggle all, <i> to invert selection,
and <enter> to proceed)
>(*) Babel
 ( ) TypeScript
 ( ) Progressive Web App (PWA) Support
 ( ) Router
 ( ) Vuex
 ( ) CSS Pre-processors
 ( ) Linter / Formatter
 (*) Unit Testing
 ( ) E2E Testing

```

Por el momento solo elegiremos Babel y Unit Testing. ***La selección se hace presionando "space"*** . 
Continuaremos presionando **"Enter"**

```shell
Vue CLI v5.0.8
? Please pick a preset: Manually select features
? Check the features needed for your project: Babel, Unit
? Choose a version of Vue.js that you want to start the project with
> 3.x
  2.x
```

A continuación elegiremos la versión 3 de Vue JS y como herramientas para test Jest

```shell
Vue CLI v5.0.8
? Please pick a preset: Manually select features
? Check the features needed for your project: Babel, Unit
? Choose a version of Vue.js that you want to start the project with 3.x
? Pick a unit testing solution: (Use arrow keys)
> Jest
  Mocha + Chai
```

Por último, el CLI nos preguntará si queremos usar un archivo dedicado para guardar esta configuración o si preferimos usar el package.json  
Elegiremos usar un **archivo dedicado**.

¡Listo! Ya tenemos nuestro primer proyecto en VueJS creado con el CLI. Ahora vamos a abrirlo y para eso al igual que el ejemplo anterior usaremos los siguientes comandos:

```shell
cd 01-first-app
npm run serve
```




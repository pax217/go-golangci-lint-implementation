<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://golangci-lint.run/">
    <img src="docs/images/golangci-lint.png" 
        alt="Logo" 
        width="500" 
        height="240">
  </a>

<h3 align="center">golangci-lint</h3>

  <p align="center">
    Una herramienta para revisar nuestro código goolang !!!
    <br />
    <a href="https://golangci-lint.run/"><strong>Explorar documentacion »</strong></a>
    <br />
    <br />
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## Acerca del Proyecto

**golanci-lint** es uma herramienta de programación que tiene como objetivo detectar codigo sospechoso, consufo o incompatible em programas escritos en C, es decir , errores de programación que se escapan al abitual análisis sintáctico que hace el compilador.

**¿Vale la pena usar linters?**

Es muy probable que algun compañero haya comentado alguna vez que los linters son engorrosos, y que terminan siendo mas molestos que útiles.

<p align="right">(<a href="#readme-top">back to top</a>)</p>


### Construida Con

Esta aplicacion golang esta construida con:

<div align="center">
  <a href="https://golangci-lint.run/">
    <img src="https://miro.medium.com/max/1400/1*Ifpd_HtDiK9u6h68SZgNuA.png" 
    alt="drone-ci" 
    width="150" 
    height="80">
    <img src="https://res.cloudinary.com/practicaldev/image/fetch/s--03aGzsK6--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/yhyydxn1t8b01l5aybpn.png" 
    alt="drone-ci" 
    width="200" 
    height="80">
  </a>
</div>


<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- GETTING STARTED -->
# Para iniciar

Es importante tomar en cuanta que debemos de tener instalado:

- drone ci 1.7.0
- go 1.19
- scoop

# Prerequisitos

## Scoop
Es un administrador de paquetes que dorne ci nos da como sugerncia para instalar nuestro CI
de forma local.

Ejecutar en Power shell

  ```sh
  Set-ExecutionPolicy RemoteSigned -Scope CurrentUser # Optional: Needed to run a remote script the first time
  ```

  ```sh
  irm get.scoop.sh | iex
  ```

## Drone CI

Drone es una herramienta robusta para la implementación de prácticas DevOps relacionadas con la integración contínua, el despliegue contínuo y la entrega continua. Al ser Container Native, Drone puede ejecutarse directamente como un servicio dentro del orquestador de contenedores

* Instalar drone
  ```sh
  scoop install drone
  ```
  
* Verificar versión de drone
  ```sh
  drone --version
  ```

## golangci-lint

linter es una herramienta de programación que tiene como objetivo detectar codigo sospechoso, consufo o incompatible em programas escritos en C, es decir , errores de programación que se escapan al abitual análisis sintáctico que hace el compilador.

## Ejecutar en Git Bash (Windows)

* Instalar golangci-lint
  ```sh
  curl -sSfL https://raw.githubusercontent.com/golangci/golangci-lint/master/install.sh | sh -s -- -b $(go env GOPATH)/bin v1.51.0
  ```

* Verificar golangci-lint
  ```sh
  golangci-lint --version
  ```

# Uso 

_Despues de haber instalado nuestras herramientas para la ejecución de liner es importante tomar en cuenta los siguiente pasos_

Esta configuración se encuentra en [golangci-lint]( golangci.yml)

1. Revisar nuestro código con golangci-lint 
   
    Este archivo contiene la configuración de los linters que se ejecutarán 
    para revisar nuestro código.

    **Importante** revisar la documentación de lo que revisa cada uno de los linters

   https://golangci-lint.run/usage/linters/

* Realizar la ejecución default que tiene 
  ```sh
  golangci-lint run
  ```

* Realizar la ejecución con la configuración en nuestro proyecto (la que usaremos)
  ```sh
  golangci-lint run --config golangci.yml
  ```
  
    Archivo de configuración : golangci.yml

2.- Simular el step en Drone CI

_Despues de haber instalado nuestras herramientas para la ejecución de drone ci es importante tomar en cuenta los siguiente pasos_

Este paso simula el paso en nuestro continus Integration de foma local,la configuración se encuentra en [.drone.yml](.drone.yml)

* Ejecución de Step Lineter (Local)
  ```sh
  drone exec --pipeline production
  ```


<!-- CONTACT -->
# Contact

Carlos Alberto Maldonado Díaz - cmaldonado@occ.com.mx.com


<p align="right">(<a href="#readme-top">back to top</a>)</p>


## Referencias

* [GopherCon 2019: Denis Isaev - Go Linters: Myths and Best Practices](https://www.youtube.com/watch?v=1U-Gzz4TYP0)
* [Linters en Go](https://blog.friendsofgo.tech/posts/linters-en-go/)
* [golangci-lint](https://golangci-lint.run/)
* [scoop](https://scoop.sh/)
* [drone-local](https://docs.drone.io/server/ha/developer-setup/)
  


<p align="right">(<a href="#readme-top">back to top</a>)</p>




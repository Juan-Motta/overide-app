# OVERIDE

Overide es un projecto orientado a mejorar los viajes terrestres intermunicipales. EL objetivo del proyecto es hacer el proceso de administracion y gestion de los itinerarios de viajes mucho mas sencillo y organizado para las compañias de viajes terrestres y hacer el proceso de busqueda y compra mas amigable y confiable para los usuarios.

El proyecto consta de dos partes, una seccion orientada al back-end y otra al front-end. En los siguientes apartados podra encontrar la documentacion asociada a los proyectos.
<ul>
  <li><a href="https://github.com/Juan-Motta/overide-backend-app/tree/main/Cliente">Documentacion Front-End</a></li>
  <li><a href="https://github.com/Juan-Motta/overide-backend-app/tree/main/Gateway%20API">Documentacion API Gateway</a></li>
  <li><a href="https://github.com/Juan-Motta/overide-backend-app/tree/main/Usuarios">Documentacion Microservicio Usuarios</a></li>
  <li><a href="https://github.com/Juan-Motta/overide-backend-app/tree/main/Trayectos">Documentacion Microservicio Trayectos</a></li>
  <li><a href="https://github.com/Juan-Motta/overide-backend-app/tree/main/Reservas">Documentacion Microservicio Reservas</a></li>
</ul>

## Arquitectura

La arquitectura utilizada para el sistema de control de reservas de la empresa de viajes es la arquitectura de 3 capas las cuales son:
<ul>
  <li>Capa de presentacion</li>
  <li>Capa de negocio</li>
  <li>Capa de datos</li>
</ul>

## Tecnologias a utilizar

<ul>
  <li>Django</li>
  <li>Express</li>
  <li>Apollo</li>
  <li>VueJS</li>
  <li>Bootstrap</li>
  <li>PostgreSQL</li>
  <li>MongoDB</li>
</ul>

## Arquitectura de microservicios

La aplicación cuenta con diferentes sub-sistemas, primero cuenta con un front-end creado en VueJS encargado de toda la capa de presentacion, tres microservicios en el lado de back-end encargados del sistema de usuarios y autenticacion, el sistema de reservas y el sistema de trayectos, estos sistemas se encuentran construios en Express para el sistema de usuarios junto con una base de datos no relacional (mongoDB) y Django Rest Framwork para los sistemas de reservas y trayectos junto con una base de datos relacional (PostgreSQL), ademas los sistemas se encuentran interconectados por un API gateway basada en GraphQL.

![Untitled Diagram drawio (5)](https://user-images.githubusercontent.com/78517969/140631339-150d7afb-c257-4d61-b5e4-ec450d69ca08.png)

## Base de datos

![Untitled Diagram drawio (5)](https://user-images.githubusercontent.com/78517969/140626965-c20435c1-264a-4627-9ef0-9d78c6461511.png)



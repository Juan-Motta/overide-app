# OVERIDE

Overide es un projecto orientado a mejorar los viajes terrestres intermunicipales. EL objetivo del proyecto es hacer el proceso de administracion y gestion de los itinerarios de viajes mucho mas sencillo y organizado para las compañias de viajes terrestres y hacer el proceso de busqueda y compra mas amigable y confiable para los usuarios.

El proyecto consta de dos partes, una seccion orientada al back-end y otra al front-end. En los siguientes apartados podra encontrar la documentacion asociada a los proyectos.
<ul>
  <li><a href="https://github.com/Juan-Motta/overide-backend-app/tree/main/Cliente">Documentacion Front-End</a></li>
  <li><a href="https://github.com/Juan-Motta/overide-backend-app/tree/main/Gateway%20API">Documentacion API Gateway</a></li>
  <li><a href="https://github.com/Juan-Motta/overide-backend-app/tree/main/Usuarios">Documentacion Microservicio Usuarios</a></li>
  <li><a href="https://github.com/Juan-Motta/overide-backend-app/tree/main/Trayectos">Documentacion Microservicio Trayectos</a></li>
  <li><a href="https://github.com/Juan-Motta/overide-backend-app/tree/main/Reservas">Documentacion Microservicio Reservas</a></li>
  <li><a href="https://github.com/Juan-Motta/overide-app/tree/main/Mail">Documentacion Microservicio Mailing</a></li>  
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

La aplicación cuenta con diferentes sub-sistemas, primero cuenta con un front-end creado en VueJS encargado de toda la capa de presentacion, cuatro microservicios en el lado de back-end los cuales son:
<ul>
  <li>Servicio de usuarios y autenticación</li>
  <li>Servicio de trayectos</li>
  <li>Servicio de reservas</li>
  <li>Servicio de correo</li>
</ul>
estos sistemas se encuentran construios en Express para el sistema de usuarios junto con una base de datos no relacional (mongoDB) para el servicio de usuarios y autenticación, Expresss y NodeMailer para el servicio de correo y Django Rest Framwork junto con una base de datos relacional (PostgreSQL) para los servicios de trayectos y reservas, ademas los sistemas se encuentran interconectados por un API gateway basada en GraphQL.

![Untitled Diagram drawio (5)](https://user-images.githubusercontent.com/78517969/140796471-df428234-502f-4e4b-839c-39cbc45341a8.png)


## Base de datos

![Base de datos drawio (1)](https://user-images.githubusercontent.com/78517969/140799006-00598580-07f0-42e0-90e3-700e802b1b4f.png)

## Descripción del proceso de reserva

El proceso de reserva de un pasaje comienza con el usuario llenando el formulario el cual contiene los campos para ingresar la ciudad de origen, de destino, la fecha y la hora del viaje, si estos datos coinciden con algun trayecto disponible en la base de datos se debe proceder a la seleccion del mismo, si los datos ingresados no coinciden se finaliza el proceso y el usuario debera buscar otro trayecto con nuevos valores. Una vez seleccionado el trayecto se comprobara si el usuario se encuentra logeado en la aplicación, si lo esta se procedera al ingreso de datos del pasajero, si no se procedera a realizar el proceso de inicio de sesion para continuar con el ingreso de datos. En el ingreso de datos del pasajero el usuario tendra que llenar todos los campos referentes a la informacion personal del pasajero y una vez terminado se procedera a la seleccion de puesto y finalmente a la confirmacion de la reserva en donde el usuario podra ver todo el resumen de la información de la reserva.

<p align="center">
  <img src="https://user-images.githubusercontent.com/78517969/140853813-a3e3eb6b-76b0-43f3-8455-f399ad808b27.png" alt="DB_Model" />
</p>



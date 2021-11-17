# OVERIDE

Overide es un projecto orientado a mejorar los viajes terrestres intermunicipales. EL objetivo del proyecto es hacer el proceso de administracion y gestion de los itinerarios de viajes mucho mas sencillo y organizado para las compañias de viajes terrestres y hacer el proceso de busqueda y compra mas amigable y confiable para los usuarios.

El proyecto consta de dos partes, una seccion orientada al back-end y otra al front-end. En los siguientes apartados podra encontrar la documentacion asociada a los proyectos.
<ul>
  <li><a href="https://github.com/Juan-Motta/overide-backend-app/tree/main/Cliente">Documentacion Front-End</a></li>
  <li><a href="https://github.com/Juan-Motta/overide-backend-app/tree/main/Gateway%20API">Documentacion API Gateway</a></li>
  <li><a href="https://github.com/Juan-Motta/overide-auth-users-microservice">Documentacion Microservicio Usuarios</a></li>
  <li><a href="https://github.com/Juan-Motta/overide-rides-microservice">Documentacion Microservicio Trayectos</a></li>
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

<p align="center">
  <img src="https://user-images.githubusercontent.com/78517969/142131583-447754a5-02c5-4cf6-983a-8fe072abb13b.png" alt="DB_Model" />
  
</p>

## Arquitectura de microservicios

La aplicación cuenta con diferentes sub-sistemas, primero cuenta con un front-end creado en VueJS encargado de toda la capa de presentacion, cuatro microservicios en el lado de back-end los cuales son:
<ul>
  <li>Servicio de usuarios y autenticación</li>
  <li>Servicio de trayectos</li>
  <li>Servicio de reservas</li>
  <li>Servicio de correo</li>
</ul>
Los cuales estan contruidos con las siguientes tecnologias:
<br>
<br>
<ul>
  <li>Servicio de usuarios y autenticación: Django + PostgreSQL</li>
  <li>Servicio de trayectos: Spring Boot + PostgreSQL</li>
  <li>Servicio de reservas: Express + MongoDB</li>
  <li>Servicio de correo: Expres + NodeMailer</li>
</ul>

![arquitectura drawio (2)](https://user-images.githubusercontent.com/78517969/142131850-724552b8-699c-4b73-a770-a28d56e88eb9.png)

## Base de datos

![Base de datos drawio (5)](https://user-images.githubusercontent.com/78517969/141704945-c69dfac5-4da7-4a68-ac1d-3e469179e299.png)

## Descripción del proceso de reserva

El proceso de reserva de un pasaje comienza con el usuario llenando el formulario el cual contiene los campos para ingresar la ciudad de origen, de destino, la fecha y la hora del viaje, si estos datos coinciden con algun trayecto disponible en la base de datos se debe proceder a la seleccion del mismo, si los datos ingresados no coinciden se finaliza el proceso y el usuario debera buscar otro trayecto con nuevos valores. Una vez seleccionado el trayecto se comprobara si el usuario se encuentra logeado en la aplicación, si lo esta se procedera al ingreso de datos del pasajero, si no se procedera a realizar el proceso de inicio de sesion para continuar con el ingreso de datos. En el ingreso de datos del pasajero el usuario tendra que llenar todos los campos referentes a la informacion personal del pasajero y una vez terminado se procedera a la seleccion de puesto y finalmente a la confirmacion de la reserva en donde el usuario podra ver todo el resumen de la información de la reserva.

<p align="center">
  <img src="https://user-images.githubusercontent.com/78517969/140853813-a3e3eb6b-76b0-43f3-8455-f399ad808b27.png" alt="DB_Model" />
</p>



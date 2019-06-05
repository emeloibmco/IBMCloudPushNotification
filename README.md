# IBMCloudPushNotification
Hands On de aplicación web que recibe notificaciones utilizando el servicio IBM Cloud Push Notification

## Índice

* Prerequisitos
* Creación servicio de Cloud Messaging en Google Firebase.
* Creación y configuración servicio Push Notification en IBM cloud.
* Creación de aplicación SDK for node.js.
* Instalación del CLI.
* Referencias.


## 1. Introducción

En la siguiente guía se podrá observar cómo se realiza la creación y ejecución de un Push Notification con ayuda de las herramientas que proporciona IBM cloud.

Va desplegar una aplicación web en NodeJS en IBM Cloud, y vamos a crear el servicio Push Notification para enviar mensajes a la aplicación, utilizando como proveedor Firebase Cloud Meesaging, como proveedor de mensajes. 


![1](https://user-images.githubusercontent.com/50923637/58977747-f14ded80-878f-11e9-81f3-6f3f7a62e812.png)

https://console.bluemix.net/docs/services/mobilepush/c_overview_push.html#overview-push 

## 2. Prerequisitos

* Acceso a Intenet.
* Acceso a IBM Cloud, para crear la aplicación ejemplo y el servicio de Push Notification. 
* Acceso a Google Firebase Cloud Messaging, para crear el proyecto y utilizar el servicio como proveedor de envio de mensajes. 
* Vamos a utilizar la linea de comando de IBM Cloud, para modificar la aplicación y hacer la configuración para el registro al servicio de Push Notification. 
* Para esto es necesario tener instalado IBM Cloud CLI, npm, NodeJS, en los computadores de los asistentes. 

**En los siguientes enlaces podrá encontrar información acerca de la CLI de IBM Cloud y acerca de NPM.**

https://cloud.ibm.com/docs/cli?topic=cloud-cli-ibmcloud-cli#ibmcloud-cli

https://www.npmjs.com/get-npm

## 3. Creación servicio de Cloud Messaging en Google Firebase

Primero para poder inicia con el proceso de creación del servicio de Cloud Messaging en Google Firebase, usted debe dirigirse al siguiente enlace https://firebase.google.com/docs/cloud-messaging/.

Al ingresar en el enlace anteriormente mencionado podrá ver la siguiente página la cual es la página del servicio de Firebase Cloud Messaging, estando situado en esta página debe dar clic en la opción ir a la consola.

![2](https://user-images.githubusercontent.com/50923637/58978589-bfd62180-8791-11e9-8f0d-e3095eb87bd4.jpg)

Luego de  acceder  a  la  consola  de  Cloud  Messaging  en  Google  Firebase,  usted  debe  crear  un  nuevo  proyecto, para hacer esto, usted debe seleccionar la opción agregar proyecto.

![3](https://user-images.githubusercontent.com/50923637/58978745-18a5ba00-8792-11e9-94db-6d372ca4d5c9.jpg)

Después de hacer seleccionado la opción de agregar nuevo proyecto le saldrá una ventana emergente en la cual usted  puede  asignarle  un  nombre  al  proyecto,  podrá  ver  la  ID  del  proyecto  que  está creando,  las  ubicaciones, no olvide seleccionar la casilla de acepto términos relativos a los controladores tal cual como esta en la imagen, finalmente debe seleccionar la opción crear proyecto dando clic en ella.

![4](https://user-images.githubusercontent.com/50923637/58978832-5276c080-8792-11e9-9241-0aab4518ca54.jpg)

Después de haber seleccionado la opción de crear proyecto podrá ver la siguiente ventana emergente en la cual le dirá que su proyecto se creó de forma exitosa, al ver ese aviso usted da clic en continuar para seguir con el resto del procedimiento.

![5](https://user-images.githubusercontent.com/50923637/58979221-260f7400-8793-11e9-9c9b-45b4853a1123.png)


## 4. Creación y configuración servicio Push Notification en IBM cloud.

Para realizar la creación y la configuración del servicio de Push Notification en IBM Cloud debe acceder a la siguiente  URL  https://cloud.ibm.com,  luego  de  acceder  a  ella  debe  dar  clic  en  la  opción  Log-in,  la  cual  lo dirigirá a una página en la cual podrá ingresar su usuario y contraseña correspondiente para ingresar al portal de IBM Cloud.

![6](https://user-images.githubusercontent.com/50923637/58979630-13e20580-8794-11e9-892d-d17c288d1822.jpg)

Luego en la página que podrá ver en la siguiente imagen ingresa su usuario y contraseña correspondiente, luego da clic en iniciar sesión, todo esto para realizar el ingreso a IBM Cloud.

![7](https://user-images.githubusercontent.com/50923637/58979679-32480100-8794-11e9-9a4e-9e9d7fb6a7ae.jpg)

Luego estando dentro del portal de IBM Cloud usted podrá ver la opción de catálogo la cual seleccionará para continuar con el proceso de creación y configuración de Push Notification.

![8](https://user-images.githubusercontent.com/50923637/58979812-7cc97d80-8794-11e9-8b4b-78ac80d41ef9.jpg)

Después dentro del catálogo podrá ver todos los servicios que provee IBM Cloud, seleccionará la opción Web y
Móvil en la parte izquierda de su pantalla podrá ver esa opción.

![9](https://user-images.githubusercontent.com/50923637/58979866-9f5b9680-8794-11e9-92dc-3f8e954f95ac.jpg)

Luego estando situado en opción web y móvil del catálogo de IBM Cloud, usted debe buscar el servicio de Push
Notification, en cual debe seleccionar dando clic en él.

![10](https://user-images.githubusercontent.com/50923637/58979908-b8fcde00-8794-11e9-88bc-7f0c2cb4b968.jpg)

Luego usted vera una página en la cual le asignara un nombre a su servicio, seleccionará la región deseada y el grupo de recursos en el que quiera que este asignado su servicio.

![11](https://user-images.githubusercontent.com/50923637/58979935-cdd97180-8794-11e9-8262-94f62c1179e5.jpg)

Luego vera  una  ventana  en  la  cual  deberá  agregar  una  nueva  credencial  para  utilizar  el  servicio  desde  una aplicación Web o Mobile.

![12](https://user-images.githubusercontent.com/50923637/58979968-e6498c00-8794-11e9-90a5-a59b8f7da50f.jpg)

La siguiente imagen muestra la configuración del servicio Push Notification.  La URL se debe agregar una vez se despliegue la aplicación en un paso posterior: 

![13](https://user-images.githubusercontent.com/50923637/58980097-33c5f900-8795-11e9-81df-184df6c6120f.jpg)

## 5. Creación de aplicación SDK for node.js.

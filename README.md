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

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

Luego dentro del catálogo debe buscar la opción SDK for Node.js, puede facilitar su proceso de búsqueda dando en  la  opción  de  búsqueda  donde  podrá  ver  una  lupa,  escribe  la  palabra  SDK  esto  le  filtrara  resultados,  luego seleccionara SDK for Node.js dando clic en él.

![14](https://user-images.githubusercontent.com/50923637/58984157-f4e87100-879d-11e9-8907-84527dee8012.jpg)

Luego creara la aplicación  SDK  for  Node.js,  la  cual  es  una  aplicación  de  Cloud  Foundry,  luego  asignara  un nombre, la ubicación de despliegue del servicio y una etiqueta si así lo desea.

![15](https://user-images.githubusercontent.com/50923637/58984236-2103f200-879e-11e9-8709-14e0e537ede7.jpg)

Después de que se realizó el despliegue de la aplicación vera la siguiente página donde le dará ingreso a la URL
de la app, esta opción es de fácil visibilidad, la opción aparee como Visitar URL de app.

![16](https://user-images.githubusercontent.com/50923637/58984272-42fd7480-879e-11e9-9114-0cd8671cb897.jpg)

Ahora usted debe realizar el proceso de configuración, para lo cual debe seleccionar la opción ’Toolchain’ cadena de herramientas,  
en esta cadena de herramientas podrá encontrar el código de la aplicación para poder modificar el código fuente.

![17](https://user-images.githubusercontent.com/50923637/58984434-b2736400-879e-11e9-86a6-e544d2795777.jpg)

Luego de acceder  a  la  cadena  de  herramientas  podrá  ver  las  herramientas que  componen  su  aplicación,  selec- cionara la herramienta Git para ir al repositorio de GitHub y descargar el código fuente de su aplicación para poder realizar modificaciones a su aplicación.

![18](https://user-images.githubusercontent.com/50923637/58984432-b2736400-879e-11e9-92b4-a7bf7273a314.jpg)

Para editar el proyecto es necesario tener un ambiente local en con herramientas de edición, preferiblemente un IDE, y con las herramientas de IBM Cloud CLI para acceder a IBM Cloud y desplegar la aplicación ejemplo en Cloud Foundry. 

Una vez se ha descargado el código fuente, descomprime el archivo.  En el ejemplo el directorio del proyecto es llamado *demo-pushnotification-master.*

En la imagen se muestra el comando para acceder a la plataforma IBM Cloud:   `ibmcloud login`

![19](https://user-images.githubusercontent.com/50923637/58984553-f6feff80-879e-11e9-96f9-5c7fe7f1cd37.jpg)

Es necesario seguir la guía en el ejemplo de Web HelloPush, para modificar la aplicación utilizando el código fuente del ejemplo: 

[IBM-bluemix-push-notifications](https://github.com/ibm-bluemix-push-notifications)/[Web_helloPush](https://github.com/ibm-bluemix-push-notifications/Web_HelloPush)

El siguiente es el resumen de las modificaciones: 

### Configuración

1. Abra el ejemplo **Example_Website**, y descargue el código de ejemplo
2. Reemplace el contenido del folder  `public` con el contenido de  `Example_Website/public`
3. Descargue y agregue las versiones más recientes de **BMSPushSDK.js** y **BMSPushServiceWorker.js** del siguiente link [Download](https://github.com/ibm-bluemix-mobile-services/bms-clientsdk-javascript-webpush)
4. Edite el archivo  `public/index.html` y agregue las credenciales de su servicio de Push notification (`line 67`).
5. Ejecute el commando `ibmcloud app push` para desplegar el proyecto en Cloud Foundry
6. Registre el nombre (**URL**) de la aplicación en la configuración del servicio de Push Notification
7. Abra el browser y acepte el registro del servicio de Push Notification
8. Envié notificaciones desde el servicio de Push Notification

Los siguientes son los segmentos de código a modificar como parte de este ejercicio, adicionando las credenciales del servicio de Push Notification: 

**public/index.html**
```
    var bmsPush = new BMSPush()
    function callback(response) {
      alert(response.response)
    }
    var initParams = {
      "appGUID":"push app GUID",
      "appRegion":"Region where service hosted",
      "clientSecret":"clientSecret of your push service",
      "websitePushIDSafari": "Optional parameter for Safari Push Notifications only. Refer Docs."
    }

    //Initialize Push
    bmsPush.initialize(initParams, callback)

    //Register Push
    bmsPush.register(function(response) {
      alert(response.response);
    })

```

**public/manifest.json**

```
{
  "name": "Push Notifications IBM",
  "gcm_sender_id": "1074675423985",
   "permissions": [
          "storage"
        ]
}

```

La siguiente es la página en donde se envía el mensaje de notificación a la aplicación cliente: 


![20](https://user-images.githubusercontent.com/50923637/58985555-3595b980-87a1-11e9-85f2-56a0e8a762c9.jpg)

## Referencias

* Web_HelloPush https://github.com/ibm-bluemix-push-notifications/Web_HelloPush
* ibm-bluemix-push-notifications https://github.com/ibm-bluemix-push-notifications/
* Video ejemplo hello world de push notification https://www.youtube.com/watch?v=qusSM8KihNE

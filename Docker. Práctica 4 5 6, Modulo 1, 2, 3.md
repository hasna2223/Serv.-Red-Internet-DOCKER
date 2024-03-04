![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/c1984f1e-1409-4c1b-bac6-1c1262179089)                                                  Docker. Práctica 4 5 6, Modulo 1, 2, 3
                                                            HASNA BIDAN 2º ASIR

Modulo 1

  Configuración

Configuración de contenedores con variables de entorno:

Crear un contenedor que necesitara una configuración específica. Para ello, crearemos variables de entorno en el contenedor, para que el proceso que inicializa el contenedor pueda realizar dicha configuración:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/11ca2efe-6b2f-41ac-b22f-14b06f7915db)

Configuración de un contenedor con la imagen mariadb:

En ocasiones, es necesario inicializar una variable de entorno clave para ejecutar un contenedor. Al revisar la documentación de la imagen mariadb en Docker Hub, notamos que algunas variables, como MYSQL_ROOT_PASSWORD, deben configurarse obligatoriamente para garantizar el correcto funcionamiento del contenedor.

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/88ca0340-5b25-45d1-a890-5b2ba7517fb3)

Podemos ver que se ha creado una variable de entorno:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/23cbc727-da8d-463a-95e9-859cfd157f5f)

ejecutaremos:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/1ba8fdf2-7d50-434c-823f-3803773ddf1d)

Para acceder: 

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/87bd5e5f-ee39-4043-8760-bb8340229dbd)

Accediendo a servidor de base de datos desde el exterior:

Vamos a mapear los puertos para acceder desde el exterior a la base de datos:
Primero, eliminar el contenedor anterior:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/946afbb6-27a3-4335-8ed2-8abafceb6561)

Crear otro contenedor, pero ahora vamos a mapear el puerto 3306 del anfitrión con el puerto 3306 del contenedor:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/198a4991-a740-46eb-9421-3ec663bfdc1d)

Comprobaremos:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/05f02fe7-6bf5-46f7-8166-f088217e68c4)

Instalamos el cliente de mariadb:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/2c52947b-a465-4da6-90bd-a7e76ef79852)

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/a8dcf035-4140-49c0-8759-b29bfb48c0f9)

Contenedor:

Ejecución simple de contenedores:
Con el comando run vamos a crear un contenedor donde vamos a ejecutar un comando:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/d081be55-fe7a-4a2c-b5a7-54f0f4a6996f)

Comprobamos con este comando:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/44e020ad-b254-49b5-95a0-7fe11f958391)

Con el comando docker images podemos visualizar las imágenes que ya tenemos descargadas en nuestro registro local:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/0c9ad5d4-7642-486e-b5b9-9bfd303b54f4)

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/2e440ce1-307f-49ba-baad-585bd306103f)

Para ver los contenedores que no se están ejecutando:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/59a24ce7-5316-4745-a7e9-f65078446dc6)

Para eliminar el contenedor podemos identificarlo con su id: o con su nombre: docker rm nombre

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/200614b3-b4ed-4338-91ff-9a7d61dfb692)


Domonio

Creando un contenedor demonio:

En esta ocasión hemos utilizado la opción -d del comando run, para que la ejecución del comando en el contenedor se haga en segundo plano:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/c9a32eac-8132-4d06-881d-4218c55902a9)

Compruebaremos lo que está haciendo el contenedor (docker logs contenedor2):

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/67493158-69a0-4bb2-ae2c-d39968c581d4)

Por último podemos parar el contenedor y borrarlo con las siguientes instrucciones:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/ca49b05f-53fe-4d72-a09b-cff46b996541)


HolaMundo 

El "Hola Mundo" de docker:

Comprobaremos que todo funciona creando nuestro primer contenedor desde la imagen helloworld:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/0e300d50-1692-433c-a740-e63f07fba544)


interactivo

Ejecutando un contenedor interactivo:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/9c05ac75-457a-4d73-a5de-f7955faf925f)

El contenedor se para cuando salimos de él. Para volver a conectarnos a él:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/dbfcd57b-e73b-4b52-afb4-5ce79c33a572)

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/b2fe1f6e-0f6e-4ce7-84b5-12ddcd730af8)

Con la orden docker restart reiniciamos el contenedor, lo paramos y lo iniciamos.

Para mostrar información de un contenedor ejecutamos docker inspect:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/0928efa9-df76-447e-9851-c23f9b4ec97c)

En realidad, todas las imágenes tienen definidas un proceso que se ejecuta, en concreto la imagen ubuntu tiene definida por defecto el proceso bash, por lo que podríamos haber ejecutado:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/48a65908-46cb-4ce9-8d02-7ec9d80c894b)


Web

Creando un contenedor con un servidor web:

Tenemos muchas imágenes en el registro público docker hub, por ejemplo podemos crear un servidor web con apache 2.4:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/a9af1d97-f377-4903-bb1c-f85efcb405dd)

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/bb9d390b-1893-4379-8376-457796db6d26)

Para acceder al log del contenedor podemos ejecutar:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/8f972314-c7de-4583-abf0-d73b1520179f)


Modulo 2 

Creacion

Todas las imágenes tiene definidas un proceso que se ejecuta por defecto, pero en la mayoría de los casos podemos indicar un proceso al crear un contenedor.

Por ejemplo en la imagen ubuntu el proceso por defecto es bash, por lo tanto podemos ejecutar el siguiente:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/132b7858-3c9b-4d53-9e2b-6d9331a42358)

Pero podemos indicar el comando a ejecutar en la creación del contenedor:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/0aa1ddbf-6646-4214-9760-818725330bb3)

Otro ejemplo: la imagen httpd:2.4 ejecuta un servidor web por defecto, por lo tanto al crear el contenedor:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/c66aab93-9035-4a70-99a6-789878b6a25c)


Dockerhub 

Las imágenes de Docker son plantillas de solo lectura, es decir, una imagen puede contener el sistema de archivo de un sistema operativo como Debian, pero esto solo nos permitirá crear los contenedores basados en esta configuración. Si hacemos cambios en el contenedor ya lanzado, al detenerlo esto no se verá reflejado en la imagen. El Registro docker es un componente donde se almacena las imágenes generadas por el Docker Engine. Puede estar instalada en un servidor independiente y es un componente fundamental, ya que nos permite distribuir nuestras aplicaciones. Es un proyecto open source que puede ser instalado gratuitamente en cualquier servidor, pero, como hemos comentado, el proyecto nos ofrece Docker Hub. El nombre de una imagen suele estar formado por tres partes: usuario/nombre:etiqueta


Gestion

Gestión de imágenes:

Para crear un contenedor es necesario usar una imagen que tengamos descargado en nuestro registro local. Por lo tanto al ejecutar docker run se comprueba si tenemos la versión indicada de la imagen y si no es así, se precede a su descarga.


Mediawiki

Ejemplo: Desplegando la aplicación mediawiki

Vamos a crear distintos contenedores usando etiquetas distintas al indicar el nombre de la imagen, posteriormente accederemos a la aplicación y podremos ver la versión instalada: En primer lugar vamos a instalar la última versión:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/d174ad5e-b0b6-44fe-8066-7243e7761e07)

Si accedemos a la ip de nuestro ordenador, al puerto 800, podemos observar que hemos instalado la versión 1.39.1

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/b5c55228-22e2-4d43-9436-372db15f75c0)


organizacion

¿Cómo se organizan las imágenes?

Cuando creamos un contenedor ocupa muy poco de disco duro, porque las capas de la imagen desde la que se ha creado se comparten con el contenedor: Veamos el tamaño de nuestra imagen ubuntu:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/73ee3c39-5750-4f73-b90c-522cf0804fd1)

Si creamos un contenedor interactivo:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/0bacec8c-6aa8-4b53-bec5-70ff68fa7afe)

Nos salimos, y a continuación visualizamos los contenedores con la opción -s (size):

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/3f2a2239-69a3-4362-9bd0-3b9e4df481d5)

Nos damos cuenta de que el tamaño real del contenedor es 0B y el virtual, el que comparte con la imagen son los 72,9MB que es el tamaño de la imagen ubuntu.
Si a continuación volvemos a acceder al contenedor y creamos un fichero

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/fdfe0581-9e42-4265-bb6f-fd6dbfd65f32)


Modulo 3

asociacion_bind_mount

Asociando almacenamiento a los contenedores: bind mount

En este caso vamos a crear un directorio en el sistema de archivo del host, donde vamos a crear un fichero index.html

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/13abe663-04ab-4846-80d3-5e21a9a201e8)

Y comprobamos que realmente estamos sirviendo el fichero que tenemos en el directorio que hemos creado:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/690cb4f5-8c45-4677-9fcf-547b8c08b752)

Eliminamos el contenedor y volvemos a crear otro con el directorio montado:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/dcfb8e61-1c80-4110-bb34-8e6263377cad)


Asociacion_volumen

Asociando almacenamiento a los contenedores: volúmenes Docker

Veamos como puedo usar los volúmenes y los bind mounts en los contenedores. Aunque dos formas de asociar el almacenamiento al contenedor nosotros vamos a usar el flag --volume o -v. Si usamos imágenes de DockerHub, debemos leer la información que cada imagen nos proporciona en su página ya que esa información suele indicar cómo persistir los datos de esa imagen, ya sea con volúmenes o bind mounts, y cuáles son las carpetas importantes en caso de ser imágenes que contengan ciertos servicios (web, base de datos etc...)

Ejemplo usando volúmenes docker:

Lo primero que vamos a hacer es crear un volumen docker:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/a6b5e142-4152-4585-8cc9-ec7f86783b47)

A continuación creamos un contenedor con el volumen asociado, usando --mount, y creamos un fichero index.html:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/2a815750-cfa8-410f-916d-e0c33bf16906)

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/cd5f01bb-e450-448a-81aa-b811a7b1fdf4)

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/5230d449-1712-4109-8ee3-7062a7edbc5e)

Después de borrar el contenedor, volvemos a crear otro contenedor con el mismo volumen asociado:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/f4868f37-8c44-4292-b979-e4c862843469)

Y podemos comprobar que no no se ha perdido la información (el fichero index.html):

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/0e611a88-91bf-4975-b2ea-a0787e439c06)



Guestbook

Ejemplo 1: Despliegue de la aplicación Guestbook

Los dos contenedores tienen que estar en la misma red y deben tener acceso por nombres (resolución DNS) ya que de principio no sabemos que ip va a coger cada contenedor. Por lo tanto vamos a crear los contenedores en la misma red:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/826791dc-6cde-4874-b7c1-7f4765327a14)

Para ejecutar los contenedores:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/1eceb6ec-71a7-464d-883f-d8f48e40131a)

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/d87504c6-79f5-4f42-afa5-3bded1c13536)

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/4487640e-9c59-46cd-998f-f6e674a4db28)

Redes en Docker

Tipos de redes en Docker

Cuando instalamos docker tenemos las siguientes redes predefinidas:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/d9333bde-6051-4024-b829-bd97871c3cc8)

Vamos a crear un contenedor interactivos con la imagen debian:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/58e377af-daf7-49df-ae82-a5074f0ad0e8)

En otra pestaña, podemos ejecutar esta instrucción para obtener la ip que se le ha asignado:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/260e00d9-164c-4b63-a6ed-0724d1323a11)

Observamos que el contenedor tiene una ip en la red 172.17.0.3/16. Además podemos comprobar que se ha creado un bridge en el host, al que se conectan los contenedores:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/d183334d-4371-4c67-a111-611e32f0778d)

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/1c9726d4-dfc5-4d26-805b-4ab518a5fe25)

Si conecto un contenedor a la red host, el contenedor ofrece el servicio que tiene configurado en el puerto de la red del anfitrión. No tiene ip propia, sino es cómo si tuviera la ip del anfitrión. Por lo tanto, los puertos son accesibles directamente desde el host. Por ejemplo:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/4b8fc01f-72f1-4736-9156-ba3526589ae7)

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/aeeb6b75-9baf-4e76-bfd6-3ce905b0bcc2)


redes_usuario

Redes definidas por el usuario

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/989021df-3853-4c3d-a474-0694c4305f18)

Como no hemos indicado ninguna configuración en la red que hemos creado, docker asigna un direccionamiento a la red:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/c6e8c0e7-d4b2-434e-aa11-b15007c320f7)

Temperaturas.

Ejemplo 2: Despliegue de la aplicación Temperaturas

Vamos a crear una red para conectar los dos contenedores:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/bb4a5cf2-659b-473a-99bf-f0588121a8a0)

Para ejecutar los contenedores:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/851d0536-bf67-4c90-9d9d-e4b9b6e36743)

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/cb84f940-355e-41ab-a23a-229711a819c5)


Tomcat

Ejemplo 4: Despliegue de tomcat + nginx

Desplegando tomcat

Antes de hacer el despliegue del primer contenedor, vamos a crear una red bridge para conectar los contenedores:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/4144909c-ddca-467a-8fd8-e9032045c079)

A continuación vamos a crear un contenedor a partir de la imagen tomcat. En la  documentación podemos ver que el directorio /usr/local/tomcat/webapps/ es donde  tenemos que poner el fichero de despliegue war (vamos a usar bind mount para montar el fichero war en el directorio). No vamos a mapear puerto porque no vamos a acceder a este contenedor desde el exterior.
Tenemos un directorio donde tenemos el fichero war (puedes encontrar estos ficheros en el 
repositorio github)


wordpress.

Ejemplo 3: Despliegue de Wordpress + mariadb

Vamos a hacer un contenedor de WordPress

Para ello primero creamos un directorio: sudo mkdir WordPress

Dentro de este directorio creamos un fichero se llama Dockerfile: sudo gedit Dockerfile

Dentro de este fichero ponemos este contenido

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/edf06441-b41a-4d12-aded-a55bfed7fd16)

Guardamos y cerrarlo.

Para ejecutarlo usamos este comando.

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/dae2e1b7-ed2d-47fb-82a1-c795afcd852f)

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/7a29cf68-9800-4c93-9daa-9bd6e6ef7291)

En el navegador ponemos http://localhost:8080 Y como veremos ya funciona correctamiente

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/267fe0c4-7ddb-49bf-8b7d-01989a8974ea)

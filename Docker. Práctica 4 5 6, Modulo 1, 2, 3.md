                                                  Docker. Práctica 4 5 6, Modulo 1, 2, 3
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



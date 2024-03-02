
                                          Docker. Práctica 2
                                          
Lleva a cabo la práctica descrita en el primer artículo

  1. Ejecuta la imagen "hello-world"
Para ello ejecutamos el siguiente comando; sudo docker run -it hellow-world

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/017c450d-5db6-45b5-b2e6-b829f5380df1)

  2. Muestra las imágenes Docker instaladas

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/f368b824-716f-4b01-ac9c-b2fb9e806cc7)

  3. Muestra los contenedores Docker

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/356de104-6e77-4da8-9120-d4cfc57ccba4)


Lleva a cabo la práctica descrita en el segundo artículo

1. Edita el fichero Dockerfile

Hacemos un contenedor WordPress, Primero creamos un directorio con el comando siguiente: sudo mkdir WordPress

Dentro de este directorio crearemos un fich: Dockerfile: sudo gedit Dockerfile

Dentroo de este fichero ponemos lo siguiente:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/062f4b95-ce83-4af2-b825-e49fd523d4ce)

2. Construye el contenedor

3. Ejecútalo

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/1c67c87a-e520-4be0-8cd2-70771868d4d4)

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/87e1c1c2-3c09-4758-be04-a9976e008019)

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/7a3961e4-9923-4466-affb-c9820b9aa5da)

Para probar  si funciona, en el navigador buscamos: http://localhost:8080

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/77fa68bd-2394-4292-a720-58872e60afc6)

4. Create una cuenta en hub.docker.com

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/af1feb69-60b5-4bfa-ac9a-0b25414091bc)

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/73925f7a-871f-4775-a85c-df7556a24c96)

5. Publícalo

Hacemos un login: docker login:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/12a00df4-b8d9-4ca9-9060-fcff667eb1ac)

Ahora publicamos nuestra imagen docker:

![image](https://github.com/hasna2223/Serv.-Red-Internet-DOCKER/assets/119622209/ea80ed33-63f9-4db0-a0eb-27862c68cffa)


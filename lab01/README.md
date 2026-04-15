# Laboratorio 01: Docker
- Autor: Richart Escobedo

# Descripción del Laboratorio
- Utilizar Docker para desplegar dos sitios web: /developers y /webapp.
- Utilice VirtualHost en el servidor web Apache HTTP Server dentro de un contenedor Docker basado en Ubuntu 24.04.
- El sitio /developers mostrará index.html que es la presentación del grupo, webstandar.html describirá un estándar web de la W3C y contact.html mostrará un formulario para contactar al grupo.
- El sitio /webapp mostrará la aplicación web desarrollada en el curso previo.
- Automatizar el despliegue de la tarea en un Dockerfile y utilizar las recomendaciones para crear la imagen y el contenedor.

## Desplegar contenedor
```bash
docker build . -t i_daw_8080
```
```bash
docker run -d --name c_daw_8080 -p 8080:80 i_daw_8080
```
## Acceso a los sitios web 
```bash
http://127.0.0.1:8080/
```
```bash
http://127.0.0.1:8080/index2.html
```
```bash
http://10.7.46.185:8080/
```
```bash
http://10.7.46.185:8080/index2.html
```

## Detener contenedor, eliminar contenedor e imagen
```bash
docker stop c_daw_8080
```
```bash
docker rm c_daw_8080
```
```bash
docker rmi i_daw_8080
```

## Crear imagen con nombre diferente de Dockerfile
```bash
docker build -f Dockerfile2 . -t i_daw_8080
```

## Detener contenedor, eliminar contenedor e imagen
```bash
docker rm -f $(docker ps -aqf "name=^c_daw_8080$") && docker rmi i_daw_8080
```

## Pantallas
![image](sitio1.png)
![image](sitio2.png)

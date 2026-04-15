# Laboratorio 01: Docker
- Autor: Richart Escobedo

# Descripción del Laboratorio
- Utilizar Docker para desplegar dos sitios web: /developers y /webapp.
- Utilice VirtualHost en el servidor web Apache HTTP Server dentro de un contenedor Docker basado en Ubuntu 24.04.
- El sitio /developers mostrará index.html que es la presentación del grupo, webstandar.html describirá un estándar web de la W3C y contact.html mostrará un formulario para contactar al grupo.
- El sitio /webapp mostrará la aplicación web desarrollada en el curso previo.
- Automatizar el despliegue de la tarea mediante un Dockerfile y utilizar las recomendaciones para crear la imagen y el contenedor.

# Entregables
- Informe de laboratorio en formato PDF a partir de una plantilla LaTeX (tarea de Classroom).
- URL pública de video de prueba de funcionamiento máx. 2 min (Formulario Google - Classroom).
- Repositorio de GitHub que contenga todo lo necesario para desplegar (clonación en clase).

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

## Rúbrica de calificación
| ítem | Descripción | Puntaje |
| :--- | :--- | :---: |
| Informe | El informe está completo, utiliza la plantilla y tiene un acabado impecable. | 5 |
| Video | El video es preciso y muestra la ejecución del contenedor en la terminal y la navegación por la aplicación web. | 2 |
| GitHub | El repositorio contiene todos los archivos necesarios para el despliegue y muestra un orden y un manejo acordes con los estándares de codificación. | 10 |
| README | El laboratorio tiene un README.md  necesario para desplegar la aplicación web. | 3 |
| Prueba[^1] | Se tomaron en cuenta todas las consideraciones y recomendaciones, lo que evidencia un trabajo en equipo. | -0 |

[^1]: El docente debe comprobar el cumplimiento de todas las consideraciones y recomendaciones, evidenciando el trabajo en equipo con responsabilidad y práctica de la ética profesional para no aplicar ninguna penalidad.


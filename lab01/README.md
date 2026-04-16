# Laboratorio 01: Docker
| Autores | Rol | Porcentaje |
| :--- | :--- | :---: |
| Richart Escobedo | Creación del archivo Dockerfile | 100% |
| Richart Escobedo | Elaboración del informe | 100% |
|  | **Total** | **100%** |

| Entregables | URL |
| :--- | :--- |
| Repositorio | https://github.com/rescobedoq/daw.git |
| Laboratorio | https://github.com/rescobedoq/daw/tree/main/lab01 |
| Informe | https://github.com/rescobedoq/daw/blob/main/lab01/DAW_lab01.pdf |
| Video | https://youtu.be/1SThw3yJy9g |

# Descripción del Laboratorio
- Utilizar Docker para desplegar dos sitios web: **/developers** y **/webapp**.
- Configurar dos VirtualHosts en el servidor web Apache HTTP Server dentro de un contenedor Docker basado en Ubuntu 24.04.
- El VirtualHost para el sitio **/developers** mostrará **index.html** que es la presentación del grupo, **webstandar.html** describirá un estándar web de la W3C y **contact.html** mostrará un formulario para contactar al grupo.
- El VirtualHost para el sitio **/webapp** mostrará la aplicación web desarrollada en el curso previo.
- Automatizar el despliegue de la tarea mediante un Dockerfile y utilizar las recomendaciones para crear la imagen y el contenedor.

# Entregables
- Informe de laboratorio en formato PDF a partir de una plantilla LaTeX (enviar en la tarea de Classroom). [DAW_lab01.pdf]
- URL pública de video de prueba de funcionamiento máx. 2 min. (Enviar sólo la URL en la tarea de Classroom). [DAW_lab01.mp4][^1]
- Repositorio de GitHub que contenga todo lo necesario para desplegar (la clonación y la revisión se harán en clase).

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

## Rúbrica de calificación[^1]
| ítem | Descripción | Puntaje |
| :--- | :--- | :---: |
| **Informe** | El informe está completo, utiliza la plantilla y tiene un acabado impecable. | 5 |
| **Video** | El video es preciso y muestra la ejecución del contenedor en la terminal y la navegación por la aplicación web. | 2 |
| **GitHub** | El repositorio contiene todos los archivos necesarios para el despliegue y muestra un orden y un manejo acordes con los estándares de codificación. | 10 |
| **Informe** | El laboratorio cuenta con un README.md necesario para desplegar la aplicación web. | 3 |
| **Prueba[^2]** | Se tomaron en cuenta todas las consideraciones y recomendaciones, lo que evidencia un trabajo en equipo. | -0 |
|  | **Total** | **20** |

Si el docente solicita un video, debe cargarse en Youtube o Drive y sólo debe entregarse la URL pública, sin que se solicite login alguno. Es recomendable incluir la URL tanto en el README.md como en el informe.

[^1]: La autocalificación es obligatoria.
[^2]: Un video debe cargarse en Youtube o Drive y sólo debe entregarse la URL pública, sin que se solicite login alguno. Es recomendable incluir la URL tanto en el README.md como en el informe.
[^3]: El docente debe comprobar el cumplimiento de todas las consideraciones y recomendaciones, evidenciando el trabajo en equipo con responsabilidad y la práctica de la ética profesional, a fin de no aplicar ninguna penalidad.

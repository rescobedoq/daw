# Laboratorio 01: Docker
- Autor: Richart Escobedo

## Desplegar contenedor
- docker build . -t i_daw_8080
- docker run -d --name c_daw_8080 -p 8080:80 i_daw_8080
- http://127.0.0.1:8080/
- http://10.7.46.185:8080/

## Detener contenedor, eliminar contenedor e imagen
- docker stop c_daw_8080
- docker rm c_daw_8080
- docker rmi i_daw_8080

# Laboratorio 01: Docker
- Autor: Richart Escobedo

## Desplegar contenedor
```bash
docker build . -t i_daw_8080
```
```bash
docker run -d --name c_daw_8080 -p 8080:80 i_daw_8080
```
- http://127.0.0.1:8080/
- http://10.7.46.185:8080/

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

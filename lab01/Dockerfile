# Basado en la distribución Alpine
FROM alpine

# Actualización, instalación y limpieza del servidor web LightHTTP
RUN apk update \
&& apk add lighttpd \
&& rm -rf /var/cache/apk/*

# Copia de archivos al DocumentRoot
# Nota: No se está utilizando VirtualHost o Alias, sólo se está copiando directamente al DocumentRoot del servidor web
COPY ./index.html /var/www/localhost/htdocs
COPY ./index2.html /var/www/localhost/htdocs

# Poner en segundo plano la ejecución del servidor web
CMD ["lighttpd","-D","-f","/etc/lighttpd/lighttpd.conf"]

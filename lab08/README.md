# Laboratorio 08 : Django REST Framework
| Autores | Rol | Porcentaje |
| :--- | :--- | :---: |
| Richart Escobedo | Creación de serializadores | 100% |
| Richart Escobedo | Creación Vistas JSON y EndPoints | 100% |
| Richart Escobedo | Elaboración del informe | 100% |
| | **Total** | **100%** |

| Entregables | URL |
| :--- | :--- |
| Repositorio | https://github.com/rescobedoq/enrollments.git |
| Video | https://youtube.com/... |
| Informe | https://github.com/rescobedoq/enrollments/blob/main/informes/DAW_lab08_admin.pdf |

# Descripción de la práctica
- Creación de serializadores de la consulta a los modelos.
- Todavía no utilizar JWT. Permitir las operaciones GET, POST, PUT y DELETE de forma anónima.
- Crear las vistas en base a los serializadores que exponen datos en JSON.
- Crear JSON anidados para devolver consultas complejas.
- Registrar EndPoints en urls.py para consumir la API REST Framework.
- Capturar capturas de pantalla del Panel de la API DRF y de los Request con un Cliente REST (Ejemplo: SoapUI o Postman). 
- Elaborar README.md.
  
# Entregables
- Informe de práctica en PDF (enviar en la tarea de Classroom). [DAW_lab08_drf.pdf]
- Video de demostración de Request: GET, POST, PUT y DELETE.
- Repositorio de GitHub que contenga los archivos, anexos e imágenes de su investigación.

## Rúbrica de calificación[^1]
| ítem | Descripción | Puntaje |
| :--- | :--- | :---: |
| **Entorno Virtual** | Uso correcto del entorno virtual en proyectos de Python. | 2 |
| **Instalación y configuración de DRF** | Realiza detalladamente los pasos para crear instalar y configurarDjango REST Framework. | 2 |
| **Serializadores** | Explica la creación de Serializadores. | 4 |
| **Vistas JSON** | Explica la creación de vistas que produce JSON. | 4 |
| **JSON anidados** | Crea Serializadores y Vistas para producir JSON anidados para consultas complejas. | 4 |
| **Informe** | El laboratorio tiene un informe que detalla todos los pasos necesarios para el desarrollo de la práctica. | 4 |
| **Prueba[^2]** | Se tomaron en cuenta todas las consideraciones y recomendaciones, lo que evidencia un trabajo en equipo. | -0 |
|  | **Total** | **20** |

Si el docente solicita un video, debe cargarse en Youtube o Drive y sólo debe entregarse la URL pública, sin que se solicite login alguno. Es recomendable incluir la URL tanto en el README.md como en el informe.

[^1]: La autocalificación es obligatoria.
[^2]: El docente debe comprobar el cumplimiento de todas las consideraciones y recomendaciones, evidenciando el trabajo en equipo con responsabilidad y la práctica de la ética profesional, a fin de no aplicar ninguna penalidad.

## Referencias
- https://www.django-rest-framework.org/
- https://www.django-rest-framework.org/api-guide/permissions/
- https://www.geeksforgeeks.org/python/adding-permission-in-api-django-rest-framework/
- https://blog.enriqueoriol.com/2015/03/django-rest-framework-serializers.html
- https://www.geeksforgeeks.org/python/serializers-django-rest-framework/

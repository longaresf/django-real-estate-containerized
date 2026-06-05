# Containerized Real Estate Platform (Django + Docker + Gunicorn)

Este repositorio contiene una plataforma de gestión de bienes raíces desarrollada en **Django**, diseñada bajo una arquitectura de microservicios contenerizados. El proyecto destaca por su preparación para entornos de producción, utilizando **Docker** para la portabilidad y **Gunicorn** como servidor de aplicaciones de alto rendimiento.

## 🚀 Capacidades Técnicas y Arquitectura de Despliegue

* **Entorno Contenerizado (Docker):** Implementación de archivos `Dockerfile` y Docker Compose para garantizar la paridad entre los entornos de desarrollo, prueba y producción.
* **Servidor de Producción Gunicorn:** Configuración de Gunicorn como interfaz de pasarela de servidor web (WSGI) para manejar múltiples peticiones concurrentes de manera eficiente.
* **Gestión de Activos y Propiedades:** Sistema robusto de backend para la administración de listados inmobiliarios, incluyendo filtrado, categorías y persistencia de datos.
* **Seguridad y Aislamiento:** Uso de contenedores para aislar las dependencias del sistema operativo, facilitando despliegues limpios y escalables en la nube (AWS, DigitalOcean, Heroku, etc.).

## 🛠️ Stack Tecnológico

* **Framework Backend:** Django 4.x / 5.x
* **Servidor WSGI:** Gunicorn
* **Contenerización:** Docker
* **Lenguaje:** Python 3.x
* **Base de Datos:** PostgreSQL dentro del contenedor.

## ⚙️ Resolución de Desafíos de Infraestructura

El desarrollo de este proyecto se enfocó en resolver problemas críticos de despliegue moderno:

1. **Portabilidad "Write Once, Run Anywhere":** Gracias a Docker, la aplicación incluye todas sus dependencias, variables de entorno y configuraciones internas, eliminando el problema de "en mi máquina sí funciona".
2. **Preparación para Tráfico Real:** Al sustituir el servidor de desarrollo de Django (`runserver`) por **Gunicorn**, la aplicación está lista para manejar procesos en paralelo y gestionar la carga de trabajo de manera profesional.
3. **Optimización de Imágenes:** Uso de imágenes base ligeras Alpine para reducir el tamaño de los contenedores y acelerar los tiempos de despliegue en CI/CD.

## 🔧 Configuración y Ejecución con Docker

Para levantar la aplicación en tu entorno local sin necesidad de instalar dependencias manualmente, sigue estos pasos:

### Prerrequisitos
* Tener instalado **Docker** y **Docker Compose**.

### Instalación y Arranque
1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/longaresf/django-real-estate-containerized.git](https://github.com/longaresf/django-real-estate-containerized.git)
   ```
2. Construir y levantar el contenedor:
  Bash
  docker-compose up --build

3. Acceder a la aplicación:
  La plataforma estará disponible en http://localhost:8000.

✒️ Autor

    Francisco Longares - Backend & DevOps Engineer - longaresf

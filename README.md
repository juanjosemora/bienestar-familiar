# bienestar-familiar
📄 README — Proyecto de API Cuidado y Bienestar Familiar
Desarrollado por: Juan José Bocanegra Mora
Programa: Técnico en Programación de Software – SENA
🟦 Nota del estudiante

Quiero aclarar que entrego este trabajo un poco tarde debido a que tuve varios problemas técnicos con la terminal, lo que me impedía ejecutar correctamente el proyecto y avanzar como debía.
Agradezco al instructor Esteban por su paciencia y por permitirme entregar esta actividad; realmente valoro su comprensión y el apoyo brindado durante el proceso.
Muchas gracias por recibirme el trabajo.
al saber que me toco solo, tuve difucultades al desarrollarlo pero lo logre 

🧩 Sistema de Gestión – API de Cuidado y Bienestar Familiar

Este proyecto es una API modular desarrollada con Django REST Framework, siguiendo buenas prácticas de desarrollo, documentación, modularidad y uso de variables de entorno.
El objetivo general es ofrecer un sistema que permita gestionar información relacionada con el cuidado familiar, bienestar y seguimiento, integrando múltiples aplicaciones independientes dentro de un mismo proyecto backend.

Cada miembro del equipo desarrolla una aplicación separada, manteniendo independencia en modelos, endpoints y lógica de negocio.

📘 Contenido del Proyecto

Proyecto base configurado con Django + Django REST Framework

Uso obligatorio de variables de entorno (.env y .env.example)

Configuración de base de datos por variables

Documentación automática con Swagger / OpenAPI

Módulo por integrante con CRUD completo

Filtros, validaciones y un endpoint personalizado

Workflow con Git basado en ramas

Integración final sobre la rama main

⚙️ Requerimientos Técnicos

✔ Django
✔ Django REST Framework
✔ django-environ (para manejo de variables)
✔ drf-yasg o drf-spectacular para Swagger
✔ Git + GitHub
✔ Python 3.10+
✔ Base de datos PostgreSQL o SQLite (según elección del equipo)

📦 Instalación y Ejecución del Proyecto
1️⃣ Clonar repositorio
git clone https://github.com/tu-equipo/cuidado-bienestar-familiar-api.git
cd cuidado-bienestar-familiar-api

2️⃣ Crear entorno virtual
python -m venv venv
source venv/bin/activate   # Linux/macOS
venv\Scripts\activate      # Windows

3️⃣ Instalar dependencias
pip install -r requirements.txt

4️⃣ Configurar variables de entorno

Crear archivo:

.env


Ejemplo de contenido:

DEBUG=True
SECRET_KEY=tu_clave_secreta
DB_NAME=basedatos
DB_USER=usuario
DB_PASSWORD=password


Existe un archivo guía:

.env.example

5️⃣ Ejecutar migraciones
python manage.py migrate

6️⃣ Ejecutar servidor
python manage.py runserver

🧱 Estructura del Proyecto
cuidado_bienestar_familiar/
│── core/                # Proyecto base
│── apps/
│     ├── familias/      # App de gestión familiar (ejemplo)
│     ├── bienestar/     # App extra de seguimiento
│── requirements.txt
│── manage.py
│── .env.example
│── README.md

🗂 Descripción de la App del Estudiante
(Ejemplo basado en tu API, si quieres lo adapto a tu app exacta)
🏠 Aplicación: familias
Modelos

Familia

nombre

dirección

cantidad_integrantes

nivel_riesgo

Integrante

familia (relación 1-N)

nombre

edad

rol en la familia

estado_salud

Endpoints implementados
Tipo	Ruta	Descripción
POST	/familias/	Crear familia
GET	/familias/	Listar familias
GET	/familias/{id}/	Detalle de familia
PUT/PATCH	/familias/{id}/	Actualizar
DELETE	/familias/{id}/	Eliminar
GET	/familias/filtrar/?riesgo=alto	Filtro obligatorio
GET	/familias/resumen/	Endpoint extra de lógica (estadísticas)
Validaciones

No permitir crear familias con más de X integrantes

Verificación personalizada de estado de salud

📊 Swagger / OpenAPI

Toda la documentación está disponible en:

/swagger/
/redoc/


Incluye:

Documentación automática

Métodos por endpoint

Ejemplos de request y response

🔀 Flujo de Trabajo con Git

Cada integrante crea su rama:
feature-nombre-app

Suben commits solo a esa rama

Hacen Pull Request hacia main

El líder revisa y aprueba

Se integra en la rama principal

🧑‍🏫 Roles del Equipo

(Ejemplo — si me dices los miembros te lo lleno completo)

Líder del proyecto

Backend – App 1

Backend – App 2

Backend – App 3

Documentación

Control de versiones

✔️ Proyecto Final

El proyecto final en main:

Se instala sin errores

Carga variables correctamente

Levanta servidor

Incluye todas las apps

Swagger funcionando

CRUD + filtros + lógica personalizada por aplicación

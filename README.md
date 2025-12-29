# Asistente clínico RAG con IA Generativa 🩺

Este proyecto es un asistente inteligente diseñado para responder preguntas sobre Guías de Práctica Clínica (Hipertensión y Diabetes Mellitus Tipo 2) utilizando RAG (Retrieval-Augmented Generation).

## Características
- **Backend:** FastAPI con LangChain y Google Gemini.
- **Frontend:** Streamlit con interfaz de chat y gestión de historial.
- **Despliegue:** Dockerizado con Docker Compose.
- **Innovación:** Orquestador de intenciones, filtros por metadatos y citas de fuentes.

## Estructura del Proyecto
main.py: Código fuente del Backend.

frontend.py: Código de la interfaz Streamlit.

ingest.py: Script para procesar PDFs y crear la base vectorial.

schemas.py: definición de clases para entradas y salidas

docker-compose.yml: Orquestación de servicios.

## Requisitos Previos
1. Tener Docker y Docker Desktop instalados.
2. Tener una API Key de Google Gemini.

## Instalación y Uso

### 1. Clonar el repositorio
git clone https://github.com/testabet/asistente-de-practicas-clinicas.git

cd challenge_final_PI

### 2. Configura la variable de entorno
Crea un archivo .env en la carpeta del proyecto y agrega la API Key de Gemini

### 3. Crea la base de datos vecorial

pip install -r requirements.txt 

python ingest.py

Utiliza el script ingest.py para cargar el contenido de los PDF
¡Cuidado! Se utilizan los nombres de los PDF y una etiqueta que representa el tema (HTA o DIABETES)
Al correr el script se cargan a la base de datos ambos documentos (siempre que se encuentren en la misma carpeta)
  
### 4. Ejecuta con Docker
Levanta el sistema con el siguiente comando:

docker-compose up --build

### 5. Acceder
Chatbot: http://localhost:8501 

API Docs: http://localhost:8000/docs

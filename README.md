# Agente Inteligente BimBam Buy

## Descripción

Este proyecto fue desarrollado para el **Challenge Alura – Agentes con IA**.

El sistema implementa un agente conversacional que responde preguntas en lenguaje natural utilizando exclusivamente la información contenida en el **Manual Operativo y de Políticas de BimBam Buy**.

La aplicación extrae automáticamente el texto del documento PDF y utiliza el modelo **Gemini 2.5 Flash** para generar respuestas fundamentadas.
**Aplicación desplegada:** https://alura-agent-hdjxwimfnq-uc.a.run.app
---

## Tecnologías utilizadas

- Python 3.11
- Streamlit
- Google Gemini API
- PyPDF
- Docker
- Google Cloud Run

---

## Estructura del proyecto

```text
.
├── app.py
├── requirements.txt
├── Dockerfile
├── README.md
├── .gitignore
└── data
    └── bimbambuy_manual_politicas.pdf
```

---

## Instalación

Instalar dependencias:

```bash
pip install -r requirements.txt
```

Configurar la variable de entorno:

```bash
export GEMINI_API_KEY="TU_API_KEY"
```

Ejecutar la aplicación:

```bash
streamlit run app.py
```

---

## Funcionamiento

1. Se carga el PDF institucional.
2. Se extrae el texto mediante PyPDF.
3. El contenido completo se envía como contexto al modelo Gemini.
4. El usuario escribe una pregunta.
5. Gemini responde únicamente utilizando la información del documento.

Si la información no existe en el manual, el agente informa que no fue encontrada.

---

## Ejemplos de preguntas

- ¿Cuántos días tengo para devolver un producto?
- ¿Qué métodos de pago acepta BimBam Buy?
- ¿Cuál es la garantía estándar?
- ¿Cómo solicito un reembolso?
- ¿Cuánto tarda un envío?

---

## Despliegue

La aplicación está preparada para ejecutarse mediante Docker y desplegarse en Google Cloud Run.

Una vez realizado el despliegue, aquí se agregará la URL pública del servicio.

---

## Autor

Saúl Enrique Mendoza Ruiz

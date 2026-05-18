# ⚛️ Tutor de Física - Bot de Discord

Este proyecto es un bot de Discord autónomo diseñado para funcionar como un tutor interactivo de Física I. A través de un chat en Discord, los estudiantes pueden hacer consultas teóricas o pedir ayuda con ejercicios, y el bot responde utilizando un contexto específico basado en la bibliografía y guías de la materia (por ejemplo, resolución de ecuaciones de Schrödinger).

El sistema no solo responde con información general, sino que busca en los apuntes proporcionados para dar explicaciones precisas y fundamentadas en el material de estudio.

## 🚀 Cómo funciona

El "cerebro" del bot está construido visualmente mediante un flujo de trabajo (workflow). Cuando un usuario envía un mensaje en Discord:
1. El sistema capta la pregunta.
2. Convierte el texto en vectores matemáticos.
3. Busca en su base de datos (los PDFs de la materia) los párrafos más relevantes para esa duda.
4. Le pasa ese contexto a la Inteligencia Artificial para que genere una respuesta clara y didáctica.

## 🛠️ Tecnologías utilizadas

Este proyecto integra varias herramientas modernas de automatización e Inteligencia Artificial:

* **[n8n](https://n8n.io/):** La plataforma de automatización (Low-Code) donde está construido todo el flujo lógico e integraciones.
* **Discord API:** Como interfaz de usuario final (Frontend) donde los alumnos interactúan mediante el chat.
* **Google Gemini (LLM & Embeddings):** El motor de inteligencia artificial que comprende el texto, procesa la física y redacta las respuestas.
* **RAG (Retrieval-Augmented Generation):** La arquitectura que permite a la IA "leer" documentos locales (nodos de *Vector Store* y *Document Loaders*) para basar sus respuestas estrictamente en los libros y guías de la materia.
* **JavaScript:** Utilizado en nodos de código dentro de n8n para formatear los mensajes y limpiar los comandos entrantes.
# Chatbot de Soporte Técnico Basado en Documentación 🤖

Un **chatbot de IA** que responde preguntas técnicas basadas en documentación, utilizando **LangChain, FAISS y Modelos de Lenguaje Grandes (LLMs)**. Este proyecto demuestra habilidades en **procesamiento de lenguaje natural (NLP), recuperación de información y despliegue de modelos generativos**.

---

## **📌 Características Clave**
✅ Carga y procesamiento de documentos (PDF, DOCX, TXT).
✅ **Búsqueda semántica avanzada** con embeddings y FAISS.
✅ **Generación de respuestas contextualizadas** usando **LLMs** (FLAN-T5).
✅ Escalable y adaptable a diferentes dominios técnicos.

---

## **🤖 Modelos de Lenguaje Grandes (LLMs) Utilizados**
Este proyecto aprovecha **LLMs** para generar respuestas precisas y detalladas basadas en el contenido de los documentos. Los LLMs son modelos de IA entrenados con grandes cantidades de texto, capaces de entender y generar lenguaje humano de manera coherente.

### **Modelos Utilizados**
| Modelo               | Tipo               | Uso en el Proyecto                                                                 |
|----------------------|--------------------|------------------------------------------------------------------------------------|
| **FLAN-T5 (google/flan-t5-base)** | Modelo de generación de texto | Genera respuestas detalladas a preguntas técnicas basadas en el contexto del documento. |
| **Sentence Transformers (all-mpnet-base-v2)** | Modelo de embeddings | Convierte fragmentos de texto en vectores para búsqueda semántica con FAISS.       |

### **¿Por qué FLAN-T5?**
- **FLAN-T5** es un modelo de **instruction tuning** (ajustado para seguir instrucciones), lo que lo hace ideal para tareas de **question-answering** y generación de respuestas contextualizadas.
- Es más eficiente que modelos como GPT-3 para tareas específicas, y su versión `base` es lo suficientemente ligera para ejecutarse en entornos con recursos limitados (como Google Colab).

### **¿Por qué Sentence Transformers?**
- **all-mpnet-base-v2** genera **embeddings** (representaciones vectoriales) de alta calidad, permitiendo buscar información relevante en los documentos incluso si las palabras clave no coinciden exactamente.

---

## **🛠 Tecnologías Utilizadas**
- **LangChain**: Framework para conectar LLMs con fuentes de datos externas.
- **FAISS (Facebook)**: Biblioteca para búsqueda eficiente de similitud en espacios vectoriales.
- **Hugging Face Transformers**: Acceso a modelos preentrenados como FLAN-T5.
- **Sentence Transformers**: Generación de embeddings para búsqueda semántica.

---

## **🔍 ¿Cómo Funcionan los LLMs en este Proyecto?**
1. **División del documento**: El texto se divide en fragmentos manejables.
2. **Generación de embeddings**: Cada fragmento se convierte en un vector usando `all-mpnet-base-v2`.
3. **Búsqueda semántica**: FAISS encuentra los fragmentos más relevantes para la pregunta.
4. **Generación de respuestas**: **FLAN-T5** recibe los fragmentos relevantes y genera una respuesta coherente y contextualizada.

---
## **💻 Ejemplo de Respuesta Generada por el LLM**
Puedes ver un ejemplo completo de la salida del chatbot en ejemplo_respuesta.txt, donde FLAN-T5 genera una respuesta detallada basada en el contexto del documento.

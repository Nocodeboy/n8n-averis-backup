```markdown
# Sube FAQS a Pinecone

## Descripción
Workflow de n8n diseñado para cargar documentos de FAQS desde Google Drive, procesarlos y almacenarlos como vectores en Pinecone usando embeddings de OpenAI. Ideal para sistemas de recuperación de información basados en RAG (Retrieval-Augmented Generation).

## Requisitos
- Cuenta y credenciales de [Google Drive API](https://developers.google.com/drive/api)
- Cuenta y credenciales de [OpenAI API](https://platform.openai.com/)
- Cuenta y credenciales de [Pinecone](https://www.pinecone.io/)
- n8n con nodos:
  - `@n8n/n8n-nodes-langchain.embeddingsOpenAi`
  - `n8n-nodes-base.googleDrive`
  - `n8n-nodes-base.manualTrigger`
  - `@n8n/n8n-nodes-langchain.textSplitterRecursiveCharacterTextSplitter`
  - `@n8n/n8n-nodes-langchain.documentDefaultDataLoader`
  - `@n8n/n8n-nodes-langchain.vectorStorePinecone`

## Instrucciones de configuración
1. Configure las credenciales de Google Drive en n8n para poder acceder a la carpeta o archivos de FAQS.
2. Configure las credenciales de OpenAI para el nodo de embeddings.
3. Configure las credenciales de Pinecone para la creación y escritura en el vector store.
4. Ajuste parámetros del splitter de texto según el tamaño y formato de sus documentos.
5. Vincule las conexiones entre nodos siguiendo el orden lógico:
   - Inicio manual → carga de documentos → división de texto → generación de embeddings → almacenamiento en Pinecone.

## Detalles de funcionamiento
- El workflow inicia con un disparador manual.
- Descarga los archivos FAQS desde Google Drive.
- Usa el document loader para preparar el contenido de los archivos.
- El texto se divide en fragmentos manejables con el nodo `textSplitterRecursiveCharacterTextSplitter`.
- Cada fragmento se convierte en un embedding vectorial mediante OpenAI embeddings.
- Los vectores se almacenan en Pinecone para permitir búsquedas semánticas rápidas y eficientes.

## Ejemplos de uso
- Actualizar la base de datos de FAQS vectorizada tras añadir o modificar documentos en Google Drive.
- Preparar el índice para un chatbot que responda preguntas frecuentes usando información actualizada.
- Integrar con sistemas RAG para mejorar la recuperación de conocimiento en tiempo real.

---

**Número de nodos:** 6  
**Categoría:** agentes-ia/rag  
**Etiquetas:** (ninguna)
```
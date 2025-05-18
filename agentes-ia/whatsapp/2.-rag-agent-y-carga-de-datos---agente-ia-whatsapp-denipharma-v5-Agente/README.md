```markdown
# 2. RAG Agent y Carga de datos - Agente IA WhatsApp Denipharma V5

## Descripción
Workflow diseñado para implementar un agente de inteligencia artificial en WhatsApp utilizando la metodología RAG (Retrieval-Augmented Generation). Permite la carga, procesamiento y consulta de datos para brindar respuestas precisas y contextualizadas en conversaciones de WhatsApp para Denipharma.

## Requisitos
- Cuenta y credenciales API de OpenAI (para nodos `openAi`, `embeddingsOpenAi`, `lmChatOpenAi`).
- Cuenta y acceso a Supabase (para almacenamiento y gestión de vectores con `supabase` y `vectorStoreSupabase`).
- Credenciales de Google Drive (para nodos `googleDriveTrigger` y `googleDrive`).
- Acceso a n8n con los nodos instalados y permisos necesarios.
- Configuración de webhook para integración con WhatsApp.

## Instrucciones de configuración
1. Importar el workflow en n8n.
2. Configurar las credenciales de OpenAI: API Key y modelo.
3. Configurar las credenciales de Supabase con URL y Anon Key.
4. Añadir credenciales de Google Drive y definir los triggers según las carpetas necesarias.
5. Ajustar parámetros de nodos específicos (e.g., `textSplitterRecursiveCharacterTextSplitter`) según volumen y formato de datos.
6. Verificar y activar el workflow.
7. Configurar el webhook de WhatsApp para redirigir mensajes entrantes al disparador del workflow.

## Detalles de funcionamiento
- Utiliza nodos Langchain para integración con OpenAI y manejo de vectores.
- Carga documentos y datos desde Google Drive, procesa y segmenta información relevante.
- Almacena embeddings en Supabase para consultas rápidas y eficientes.
- Maneja memoria y contexto en conversaciones dinámicas mediante buffers.
- Incluye lógica condicional, control de flujo y ejecución por lotes para optimizar el rendimiento.
- Actúa como agente conversacional conectado a WhatsApp, respondiendo consultas con información actualizada de Denipharma.

## Ejemplos de uso
- Un usuario envía una consulta sobre un producto de Denipharma a través de WhatsApp.
- El workflow procesa la consulta, recupera datos relevantes desde la base vectorial en Supabase.
- Genera una respuesta contextualizada usando OpenAI y la envía de vuelta al usuario en tiempo real.
- Permite actualizar la base documental cargando archivos desde Google Drive, manteniendo el agente siempre actualizado.

---

**Categoría:** agentes-ia/whatsapp  
**Número de nodos:** 50  
**Etiquetas:** Agente, Denipharma, RAG
```
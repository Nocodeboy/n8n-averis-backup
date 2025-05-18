```markdown
# Agente IA Avanzado para Telegram Ecommerce

## Descripción  
Workflow avanzado que integra un agente de IA para gestionar interacciones en Telegram enfocadas en ecommerce. Utiliza modelos de lenguaje de OpenAI junto con herramientas de Google Sheets y vectores para ofrecer respuestas inteligentes, gestión dinámica y soporte personalizado en chats de Telegram.

## Requisitos  
- Credenciales de OpenAI (para nodos `openAi`, `lmChatOpenAi`, `embeddingsOpenAi`)  
- API y credenciales de Telegram (bot configurado)  
- Acceso a Google Sheets con permisos para la hoja correspondiente  
- Supabase configurado para vector store (embedding storage)  
- n8n con nodos de LangChain instalados  
- Acceso y permisos para ejecutar workflows y agentes dentro de n8n  

## Instrucciones de configuración  
1. **Configurar Telegram**:  
   - Crear un bot en Telegram y obtener el token.  
   - Establecer el webhook si es necesario.  

2. **Configurar OpenAI**:  
   - Obtener claves API de OpenAI y añadirlas en las credenciales de n8n.  

3. **Configurar Google Sheets**:  
   - Crear o utilizar una hoja existente para registrar datos/ecommerce.  
   - Conectar la credencial Google Sheets en n8n.  

4. **Configurar Supabase**:  
   - Crear un proyecto Supabase.  
   - Configurar la tabla para el almacenamiento vectorial.  
   - Añadir las credenciales a n8n.  

5. **Importar este workflow en n8n** y conectar los nodos con las credenciales configuradas.  

## Detalles de funcionamiento  
- El workflow se inicia con un disparador de Telegram (`telegramTrigger`) que captura mensajes entrantes.  
- Mediante nodos de análisis y memoria (`memoryBufferWindow`, `vectorStoreSupabase`), el agente entiende el contexto y consulta información relevante.  
- Utiliza cadenas y agentes LangChain para generar respuestas inteligentes y estructuradas (`chainLlm`, `agent`, `outputParserStructured`).  
- Emplea nodos de Google Sheets para gestionar datos de productos, pedidos o información dinámica.  
- Contiene lógica de decisión (`switch`, `if`) para distintas rutas y acciones según la conversación.  
- Respuestas y notificaciones se envían de regreso con el nodo `telegram`.  
- El agente puede ejecutar subtareas o llamar otros workflows mediante `toolWorkflow` y gestionar su vector store con `toolVectorStore`.  

## Ejemplos de uso  
- Un cliente pregunta por disponibilidad y precios de productos específicos en el catálogo.  
- Seguimiento de pedidos mediante consultas directas en el chat.  
- Soporte automatizado para resolver dudas frecuentes y redirigir casos complejos a agentes humanos.  
- Registro y actualización automática de datos en Google Sheets a partir de interacciones.  

---

**Etiquetas:** Telegram, Agente, Test  
**Categoría:** agentes-ia/telegram  
**Nodos utilizados:** 25  
```
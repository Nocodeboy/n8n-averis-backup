```markdown
# Automatización Avanzada de Prospección

## Descripción
Workflow avanzado para la generación y cualificación automática de leads, optimizando procesos de prospección en ventas mediante integración con LinkedIn y análisis inteligente de datos.

## Requisitos
- n8n vX.X o superior
- Credenciales configuradas para:
  - Airtable (API Key)
  - Google Gemini API (para `lmChatGoogleGemini`)
  - LangChain (configuración de cadenas LLM)
  - Webhook URL pública para capturar eventos externos
- Acceso a LinkedIn (si aplica acceso mediante API o integración externa)
  
## Instrucciones de configuración
1. Importar el workflow en n8n.
2. Configurar credenciales de Airtable, Google Gemini y LangChain en n8n.
3. Ajustar parámetros en nodos `set` y `code` según datos y segmentación deseada.
4. Definir y publicar el Webhook para recibir datos de entrada.
5. Verificar la correcta conexión y autenticación en cada nodo utilizado.

## Detalles de funcionamiento
Este workflow utiliza 73 nodos distribuidos para cubrir toda la lógica del proceso:
- Discriminación de leads con nodos `switch` e `if`.
- Interacción con modelos de lenguaje GPT mediante nodos LangChain (`lmChatGoogleGemini`, `chainLlm`).
- Extracción y análisis de información con `informationExtractor`.
- Gestión y almacenamiento de leads en Airtable.
- Procesamiento en lotes y segmentación con `splitInBatches` y `splitOut`.
- Manejo de eventos externos mediante Webhook.
- Codificación personalizada y notas internas para trazabilidad (`code`, `stickyNote`).

La automatización facilita la captación, filtrado y enriquecimiento de leads, agilizando la prospección y maximizando conversiones.

## Ejemplos de uso
- Captura automática de leads provenientes de campañas LinkedIn.
- Calificación dinámica y enriquecimiento mediante IA conversacional.
- Almacenamiento ordenado y segmentado de prospectos en Airtable.
- Seguimiento automatizado con respuestas personalizadas basadas en contexto.

---

**Etiquetas:** ***** | LeadGen | LinkedIn  
**Categoría:** ventas/lead-generation  
**Nodos usados:** 73  
```
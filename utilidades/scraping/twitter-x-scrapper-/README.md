```markdown
# Twitter X Scrapper

## Descripción
Workflow para extraer y procesar información de Twitter (X) mediante scraping, almacenando los datos en Google Sheets para facilitar su análisis y seguimiento.

## Requisitos
- Credenciales de Google Sheets configuradas en n8n.
- Acceso a la API pública o endpoints web de Twitter/X para scraping mediante HTTP Requests.
- Permisos para ejecutar workflows en n8n.

## Instrucciones de configuración
1. Importa el workflow en tu instancia de n8n.
2. Configura las credenciales de Google Sheets en n8n.
3. Revisa y adapta las URLs y parámetros en los nodos de `HTTP Request` para adaptarse a la estructura de Twitter/X actual.
4. Personaliza los límites y condiciones en los nodos `Limit` e `If` según tus necesidades.
5. Guarda y activa el workflow.

## Detalles de funcionamiento
El workflow inicia con un trigger manual para iniciar el scraping. Utiliza `HTTP Request` para obtener contenido de Twitter/X, procesa la información con nodos `Code` y `Set`, evalúa condiciones mediante `If` y limita operaciones con el nodo `Limit`. Los datos resultantes se almacenan en Google Sheets utilizando el nodo `Google Sheets`. Elementos como `NoOp` y `Sticky Note` están incluidos para organización y control del flujo.

## Ejemplos de uso
- Extraer tweets de un usuario específico y almacenarlos para análisis histórico.
- Monitorizar hashtags y guardar menciones relevantes en hojas de cálculo.
- Filtrar y exportar tweets basados en condiciones personalizadas para reportes periódicos.
```
```markdown
# Respuesta a emails de candidaturas

## Descripción
Workflow para automatizar la respuesta a emails relacionados con candidaturas, optimizando la gestión de procesos de selección mediante integración con Google Sheets y generación de respuestas inteligentes con OpenAI.

## Requisitos
- Credenciales de Google Sheets (para acceso y monitorización de hojas).
- Credenciales de Gmail (para envío de correos).
- API Key de OpenAI (para generación de respuestas mediante el nodo LangChain).
- Cuenta en n8n con acceso a los nodos utilizados.

## Instrucciones de configuración
1. **Google Sheets**
   - Configurar el trigger `googleSheetsTrigger` para monitorear la hoja con datos de candidaturas.
   - Asegurar que la cuenta tenga permisos de lectura/escritura sobre la hoja.
2. **Gmail**
   - Añadir credenciales que permitan enviar correos.
3. **OpenAI**
   - Configurar la API Key en el nodo `@n8n/n8n-nodes-langchain.openAi`.
4. **Condicionales**
   - Ajustar el nodo `if` según criterios específicos para decidir cuándo enviar respuestas.
5. Importar el workflow en n8n y conectar todos los nodos según configuración predeterminada.

## Detalles de funcionamiento
- El workflow se activa con cambios o nuevas filas en Google Sheets.
- Evalúa la información utilizando una condición lógica (`if`) para determinar candidaturas a responder.
- Genera respuestas personalizadas con OpenAI.
- Envía emails automáticos a través de Gmail con las respuestas generadas.

## Ejemplos de uso
- Responder automáticamente a candidatos que hayan completado cierta etapa del proceso.
- Enviar mensajes personalizados según criterios definidos en la hoja de cálculo.
- Gestionar grandes volúmenes de correos de forma eficiente y rápida.

---

**Categoría:** productividad/tareas  
**Nodos utilizados:** @n8n/n8n-nodes-langchain.openAi, googleSheetsTrigger, googleSheets, if, gmail  
**Etiquetas:** RRHH  
**Número de nodos:** 5
```
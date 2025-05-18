```markdown
# Formulario y envío de email curriculums

## Descripción
Workflow diseñado para recopilar currículums mediante un formulario, procesar y extraer información relevante, interactuar con un modelo de lenguaje para analizar o clasificar datos, y enviar los currículums vía email automáticamente.

## Requisitos
- Credenciales de Google Sheets (acceso a la hoja de cálculo para almacenar datos)
- Credenciales de Google Gmail (para el envío de emails)
- Acceso y configuración de la API de Google Gemini (modelo de lenguaje a través de Google Cloud)
- Cuenta y permisos para n8n con los nodos instalados:
  - `n8n-nodes-base.googleSheets`
  - `@n8n/n8n-nodes-langchain.lmChatGoogleGemini`
  - `@n8n/n8n-nodes-langchain.chainLlm`
  - `n8n-nodes-base.formTrigger`
  - `n8n-nodes-base.extractFromFile`
  - `n8n-nodes-base.gmail`

## Instrucciones de configuración
1. Configure las credenciales de Google Sheets en n8n con acceso a la hoja donde se guardarán los datos.
2. Configure las credenciales de Gmail para permitir el envío de emails.
3. Configure la integración con Google Gemini, asegurándose de que el API Key o credenciales necesarias estén correctamente instalados en n8n.
4. Personalice el formulario (nodo `formTrigger`) para recopilar la información deseada y aceptar el archivo del currículum.
5. Establezca la hoja de cálculo en Google Sheets para almacenar los datos recibidos.
6. Configure el nodo de extracción (`extractFromFile`) para procesar currículums en el formato esperado.
7. Verifique y ajuste el flujo de trabajo de análisis mediante los nodos `lmChatGoogleGemini` y `chainLlm` según el caso de uso.
8. Configure destinatarios, asunto y cuerpo del email en el nodo `gmail` para enviar currículums procesados.

## Detalles de funcionamiento
- El workflow se activa mediante un formulario que recibe datos y archivos (currículums).
- Los datos son almacenados en Google Sheets para seguimiento y registro.
- El nodo de extracción procesa el contenido del archivo adjunto para extraer texto relevante.
- Los nodos de lenguaje (`lmChatGoogleGemini` y `chainLlm`) analizan o clasifican el contenido del currículum de acuerdo con la lógica configurada.
- Finalmente, se envía un email con el currículum y la información procesada al destinatario definido.

## Ejemplos de uso
- Recopilar y centralizar solicitudes de empleo en Google Sheets.
- Automatizar la revisión preliminar de currículums con análisis de lenguaje.
- Enviar automáticamente los currículums a un departamento de RRHH vía email para seguimiento.

---

**Número de nodos:** 7  
**Categoría:** utilidades/integraciones  
**Etiquetas:** _(no definidas)_
```
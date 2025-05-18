```markdown
# Creación de videos virales en automático

## Descripción
Workflow de n8n diseñado para automatizar la creación de videos virales orientados a marketing de contenido. Combina procesamiento de datos, generación de texto e integración con Google Sheets y Google Drive para producir contenido optimizado y listo para difusión.

---

## Requisitos
- Credenciales de Google Sheets con acceso a las hojas usadas.
- Credenciales de Google Drive para almacenamiento y gestión de archivos.
- API Key de OpenAI para los nodos de lenguaje natural (`lmChatOpenAi`, `openAi`, etc.).
- n8n instalado con los nodos:
  - `n8n-nodes-base.googleSheets`
  - `@n8n/n8n-nodes-langchain.lmChatOpenAi`
  - `@n8n/n8n-nodes-langchain.openAi`
  - `n8n-nodes-base.googleDrive`
  - `n8n-nodes-base.merge`
  - `@n8n/n8n-nodes-langchain.chainLlm`
  - `n8n-nodes-base.code`
  - `n8n-nodes-base.scheduleTrigger`
  - `n8n-nodes-base.stickyNote`
  - `n8n-nodes-base.set`
  - `n8n-nodes-base.httpRequest`
  - `@n8n/n8n-nodes-langchain.outputParserItemList`
  - `n8n-nodes-base.wait`

---

## Instrucciones de configuración
1. Importar el workflow a n8n.
2. Configurar las credenciales de Google Sheets y Google Drive.
3. Añadir la API Key de OpenAI en los nodos correspondientes.
4. Ajustar el `scheduleTrigger` para definir la frecuencia de ejecución.
5. Revisar hojas y carpetas de Google para enlazar con la estructura del workflow.
6. Personalizar variables y parámetros según el contenido deseado.

---

## Detalles de funcionamiento
- El workflow se activa según la programación definida.
- Extrae datos y temas desde Google Sheets.
- Utiliza modelos de lenguaje de OpenAI para generar textos y guiones.
- Responsable de combinar y validar la información mediante nodos de merge y código personalizado.
- Crea archivos y los almacena en Google Drive.
- Gestiona esperas y ciclos con nodos de espera para procesos asincrónicos.
- Ofrece notas y estados mediante nodos stickyNote para seguimiento interno.

---

## Ejemplos de uso
- Automatizar la creación semanal de scripts para videos virales.
- Generar listas optimizadas para publicaciones en redes sociales.
- Integrar con plataformas externas mediante solicitudes HTTP para ampliar los recursos del contenido.
- Supervisar y modificar el flujo mediante notas adheridas y parámetros configurables.

---

**Categoría:** marketing/contenido  
**Etiquetas:** Blotato, *****  
**Número de nodos:** 46
```
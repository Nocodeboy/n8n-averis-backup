```markdown
# Extracción de datos de facturas desde email con lamaparse

## Descripción
Workflow diseñado para extraer automáticamente datos relevantes de facturas recibidas por email utilizando Lamaparse, procesar la información y almacenarla en Google Sheets para su análisis y gestión eficiente.

## Requisitos
- Cuenta de Google con acceso a Google Sheets API y credenciales configuradas en n8n.
- Cuenta de Gmail configurada con acceso IMAP para el nodo `gmailTrigger` y `gmail`.
- Clave API de OpenAI para los nodos de Langchain (`chainLlm`, `lmOpenAi`, `outputParserStructured`).
- Acceso a n8n con los nodos mencionados instalados y autorizados.

## Instrucciones de configuración
1. Configurar credenciales de Gmail en n8n para permitir la lectura y envío de emails.
2. Configurar credenciales de Google Sheets en n8n apuntando a la hoja donde se almacenarán los datos.
3. Ingresar la API Key de OpenAI en las credenciales de Langchain.
4. Ajustar los filtros del nodo `gmailTrigger` para captar únicamente emails con facturas.
5. Revisar y configurar las hojas y rangos en Google Sheets según el caso de uso.
6. Validar endpoints y parámetros en el nodo `httpRequest` según la versión de Lamaparse o servicios asociados.

## Detalles de funcionamiento
- El nodo `gmailTrigger` monitorea la bandeja de entrada en búsqueda de emails con facturas.
- Se utiliza Lamaparse a través de Langchain y nodos `lmOpenAi` para interpretar y extraer los datos clave de cada factura.
- Los datos extraídos se transforman, validan y separan con nodos como `splitOut`, `switch`, `if` y `merge`.
- Finalmente, la información estructurada se escribe en Google Sheets mediante el nodo correspondiente.
- El workflow incorpora también nodos de espera (`wait`) y notas adhesivas (`stickyNote`) para control y documentación interna.

## Ejemplos de uso
- Automatizar la contabilización y registro de facturas recibidas por email sin intervención manual.
- Consolidar información de pagos y proveedores en un solo documento accesible para el equipo.
- Integrar con sistemas de facturación o ERP mediante extensiones del workflow y nodos httpRequest adicionales.

---

**Número de nodos:** 26  
**Categoría:** utilidades/scraping  
**Nodos principales:**  
`googleSheets`, `aggregate`, `switch`, `merge`, `gmailTrigger`, `chainLlm`, `if`, `gmail`, `stickyNote`, `set`, `outputParserStructured`, `splitOut`, `httpRequest`, `lmOpenAi`, `wait`
```
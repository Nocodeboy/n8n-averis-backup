```markdown
# 2. Joe - Lead Research Tool

## Descripción
Workflow diseñado para automatizar la generación y enriquecimiento de leads de ventas, combinando herramientas de inteligencia artificial, hojas de cálculo y correo electrónico para optimizar la gestión y el seguimiento de prospectos.

## Requisitos
- Credenciales de OpenAI para el nodo `@n8n/n8n-nodes-langchain.openAi`
- Acceso a Google Sheets con permisos de escritura y lectura
- Cuenta Gmail configurada con acceso SMTP/IMAP a través del nodo `n8n-nodes-base.gmail`
- Conexión a internet para nodos que realizan solicitudes HTTP (`httpRequest`)

## Instrucciones de configuración
1. Configura las credenciales de OpenAI en n8n.
2. Conecta y autoriza tu cuenta de Google Sheets.
3. Vincula tu cuenta de Gmail para el envío y recepción de correos.
4. Ajusta las variables y parámetros en los nodos `set` y `code` según tus necesidades específicas.
5. Importa el workflow y realiza una prueba con datos reales para validar su funcionamiento.

## Detalles de funcionamiento
- Usa OpenAI para investigar y enriquecer información de leads.
- Registra y actualiza la información en Google Sheets.
- Genera contenido HTML para visualización y reportes.
- Envía correos personalizados vía Gmail para outreach.
- Utiliza notas adhesivas (stickyNote) para seguimiento interno.
- Controla el flujo mediante triggers y nodos de ejecución condicional.
- Realiza peticiones HTTP para integraciones externas adicionales.

## Ejemplos de uso
- Automatización de la captación de prospectos en procesos de ventas B2B.
- Enriquecimiento automático de bases de datos de clientes potenciales.
- Generación y envío de campañas de correo personalizadas con seguimiento integrado.
- Creación de reportes dinámicos para equipos de ventas.

---

**Número de nodos:** 20  
**Categoría:** ventas / lead-generation  
**Nodos utilizados:**  
`@n8n/n8n-nodes-langchain.openAi`, `n8n-nodes-base.googleSheets`, `n8n-nodes-base.html`, `n8n-nodes-base.code`, `n8n-nodes-base.gmail`, `n8n-nodes-base.stickyNote`, `n8n-nodes-base.executeWorkflowTrigger`, `n8n-nodes-base.set`, `n8n-nodes-base.httpRequest`
```
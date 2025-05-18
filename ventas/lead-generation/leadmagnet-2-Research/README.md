```markdown
# leadmagnet 2

## Descripción
Workflow orientado a la generación de leads dentro de procesos de ventas, automatizando la captura y procesamiento de información relevante para campañas de marketing y seguimiento.

## Requisitos
- Credenciales para acceso a n8n (según configuración del trigger).
- API externa para consultas HTTP (configurada en el nodo `HTTP Request`).
- Permisos para ejecutar workflows dentro de n8n.

## Instrucciones de configuración
1. Configure las credenciales necesarias para el nodo `Execute Workflow Trigger`.
2. Actualice la URL y parámetros en el nodo `HTTP Request` según la API utilizada para obtener o enviar datos.
3. Ajuste los campos del nodo `Set` para definir el formato y contenido de los datos que se procesarán.

## Detalles de funcionamiento
- **Execute Workflow Trigger**: Activa el workflow ante un evento o condición específica.
- **Set**: Define y organiza los datos recogidos para su procesamiento o envío.
- **HTTP Request**: Realiza peticiones a APIs externas para consultar o enviar información relevante a la generación de leads.

## Ejemplos de uso
- Capturar datos de formularios web y enviar consultas a un servicio externo para validar leads.
- Automatizar campañas de seguimiento enviando información de contacto a plataformas CRM.
- Integrar con herramientas de investigación de mercado para enriquecer perfiles de prospectos.

---

**Categoría:** ventas/lead-generation  
**Etiquetas:** Research  
**Nodos utilizados:** 3 (Execute Workflow Trigger, Set, HTTP Request)
```
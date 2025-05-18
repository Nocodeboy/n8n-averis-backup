```markdown
# 8. Joe - Opt Out Link

## Descripción  
Workflow diseñado para gestionar solicitudes de baja (opt out) a través de un enlace, integrando recepción vía webhook, actualización en Google Sheets y respuesta automática al usuario.

## Requisitos  
- Credenciales configuradas para Google Sheets en n8n.  
- URL pública para recepción del webhook (puede ser mediante n8n.cloud o servidor con acceso externo).

## Instrucciones de configuración  
1. Configurar el webhook para recibir solicitudes de opt out.  
2. Conectar y autenticar la credencial de Google Sheets apuntando a la hoja donde se registran las bajas.  
3. Ajustar el nodo `Set` para definir los campos y valores que se actualizarán o insertarán.  
4. Configurar el nodo `Respond to Webhook` para enviar confirmación al usuario.  

## Detalles de funcionamiento  
- El workflow inicia con un nodo `Webhook` que recibe la solicitud de opt out.  
- El nodo `Set` prepara los datos necesarios para la actualización.  
- Se actualiza o añade un registro en Google Sheets mediante el nodo correspondiente.  
- Finalmente, `Respond to Webhook` envía una respuesta confirmando el proceso al cliente.

## Ejemplos de uso  
- Un usuario hace clic en un enlace de baja en un correo y envía una solicitud que se registra automáticamente.  
- Seguimiento automático de solicitudes de baja con registro instantáneo en Google Sheets.  

---

**Categoría:** ventas/seguimiento  
**Número de nodos:** 4  
**Tipos de nodos:**  
- n8n-nodes-base.set  
- n8n-nodes-base.respondToWebhook  
- n8n-nodes-base.googleSheets  
- n8n-nodes-base.webhook
```
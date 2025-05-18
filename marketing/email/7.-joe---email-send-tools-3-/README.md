```markdown
# 7. Joe - Email send Tools 3

## Descripción  
Workflow diseñado para automatizar el envío masivo de correos electrónicos, integrando datos desde Google Sheets y controlando el flujo con nodos de lógica y espera para optimizar campañas de marketing por email.

## Requisitos  
- Credenciales configuradas en n8n para:
  - Google Sheets API  
  - Gmail API  
- Acceso a la hoja de cálculo con los datos de destinatarios y contenido  
- Permisos adecuados para enviar correos desde la cuenta Gmail configurada  

## Instrucciones de configuración  
1. En n8n, configure las credenciales para Google Sheets y Gmail en **Credenciales** > **Google API** y **Gmail API**.  
2. Edite el nodo de Google Sheets para apuntar al archivo y hoja correcta con la lista de contactos y contenido.  
3. Ajuste el nodo **scheduleTrigger** para definir la frecuencia de envío deseada.  
4. Configure las condiciones en los nodos **switch** e **if** para segmentar o filtrar destinatarios según su lógica de campaña.  
5. Revise y adapte el contenido en los nodos **set** para personalizar los emails antes del envío.  

## Detalles de funcionamiento  
- El workflow se ejecuta de forma programada (scheduleTrigger).  
- Obtiene los datos de destinatarios y contenido desde Google Sheets.  
- Utiliza nodos condicionales (switch, if) para segmentar destinatarios y controlar flujos.  
- Maneja la ejecución en lotes con splitInBatches y merge para escalabilidad.  
- Emplea nodos wait para espaciar envíos y evitar límites de API o spam.  
- Finaliza enviando correos personalizados a través de Gmail.  

## Ejemplos de uso  
- Envío semanal de newsletters personalizados según la segmentación.  
- Campañas de email marketing con control de frecuencias y pausas automáticas.  
- Recuperación de datos dinámicos desde Google Sheets para adaptar mensajes en tiempo real.  

---

**Número de nodos:** 30  
**Categoría:** marketing/email  
**Tipos de nodos:**  
- n8n-nodes-base.googleSheets  
- n8n-nodes-base.switch  
- n8n-nodes-base.merge  
- n8n-nodes-base.if  
- n8n-nodes-base.scheduleTrigger  
- n8n-nodes-base.gmail  
- n8n-nodes-base.set  
- n8n-nodes-base.splitInBatches  
- n8n-nodes-base.wait  
```
```markdown
# 5. Joe - Email send Tool 1

## Descripción
Workflow para gestionar y enviar campañas de email de forma automatizada, integrando datos desde Google Sheets y enviando correos personalizados vía Gmail.

## Requisitos
- Credenciales de Google Sheets para acceso a las hojas de cálculo.
- Credenciales de Gmail para envío de correos electrónicos.
- API habilitada para Gmail y Google Sheets en Google Cloud Console.
- n8n configurado con acceso a los nodos base requeridos.

## Instrucciones de configuración
1. Configure las credenciales de Google Sheets en n8n.
2. Configure las credenciales de Gmail en n8n.
3. Prepare una hoja en Google Sheets con la lista de destinatarios y datos necesarios.
4. Ajuste los parámetros en el nodo `switch` para segmentar o condicionar envíos.
5. Programe el disparador de acuerdo a la frecuencia deseada en el nodo `scheduleTrigger`.

## Detalles de funcionamiento
- El workflow inicia con un disparador basado en horario (`scheduleTrigger`).
- Extrae datos de destinatarios desde Google Sheets (`googleSheets`).
- Segmenta los datos usando un nodo `switch` para condicionar diferentes flujos.
- Divide la lista en lotes mediante `splitInBatches` para control de envío.
- Espera controlada entre envíos con el nodo `wait` para evitar bloqueos.
- Envía correos personalizados mediante el nodo `gmail`.
- Contiene un total de 15 nodos que gestionan el flujo completo de la campaña.

## Ejemplos de uso
- Envío semanal de newsletters a suscriptores segmentados.
- Campañas promocionales con envío escalonado para respetar límites de envío.
- Seguimiento automatizado de contactos según respuestas o criterios definidos.
```
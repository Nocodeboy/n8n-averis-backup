```markdown
# 6. Joe - Email send Tool 2

## Descripción  
Workflow automatizado para campañas de email marketing que gestiona la obtención de datos desde Google Sheets, procesa las condiciones de envío y envía correos personalizados mediante Gmail, optimizando envíos masivos con control de lotes y tiempos de espera.

## Requisitos  
- Credenciales válidas de Google Sheets con acceso a las hojas de datos.  
- Credenciales de Gmail con permisos para enviar correos.  
- Acceso a internet para llamadas HTTP si utiliza APIs externas.  
- Cuenta y configuración en n8n con nodos mencionados disponibles.

## Instrucciones de configuración  
1. Configure las credenciales de Google Sheets en n8n con acceso a las hojas necesarias.  
2. Configure las credenciales de Gmail para permitir el envío de correos.  
3. Ajuste los parámetros en los nodos `Set` y `Code` para personalizar mensajes y condiciones.  
4. Establezca el trigger de programación (`Schedule Trigger`) con la frecuencia deseada.  
5. Verifique y configure cualquier llamada externa en el nodo `HTTP Request`.  
6. Ajuste los límites de envío y tiempos de espera según la capacidad y políticas de Gmail.

## Detalles de funcionamiento  
- El workflow inicia su ejecución mediante un disparador programado.  
- Extrae datos de Google Sheets para obtener destinatarios y variables de correo.  
- Utiliza nodos `Switch`, `If` y `Code` para evaluar condiciones y personalizar mensajes.  
- Divide y gestiona el envío en lotes con `SplitInBatches` para evitar bloqueos y saturación.  
- Envía los emails mediante el nodo `Gmail`.  
- Implementa esperas controladas con el nodo `Wait` para respetar límites de envío.  
- Combina respuestas y controla el flujo con nodos `Merge` para finalizar el proceso.

## Ejemplos de uso  
- Envío diario de promociones personalizadas a una lista de suscriptores.  
- Campañas segmentadas que envían diferentes contenidos según atributos del usuario.  
- Reenvío automático a contactos que no abrieron el correo en envíos previos.  
- Integración con APIs externas para enriquecer datos antes del envío.

---

*Número de nodos: 33*  
*Categoría: marketing/email*  
*Tipos de nodos: Google Sheets, Switch, Merge, If, Code, Schedule Trigger, Gmail, Set, SplitInBatches, HTTP Request, Wait*  
```
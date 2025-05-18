```markdown
# 1. Investigación Pre-Llamadas de venta - Sistema de Onboarding Averis

## Descripción
Workflow diseñado para automatizar el proceso de investigación previa a llamadas de venta en el sistema de onboarding de Averis. Permite la generación y validación de leads, gestión de agendas y envío de información relevante para optimizar el contacto con prospectos.

## Requisitos
- Credenciales para:
  - OpenAI (a través del nodo `@n8n/n8n-nodes-langchain.openAi`)
  - Gmail API
  - Google Calendar API
  - Clearbit API
  - Calendly API
- Acceso a n8n con permisos para ejecutar nodos mencionados
- Configuración previa de credenciales en n8n para cada servicio

## Instrucciones de configuración
1. Importar el workflow a tu instancia de n8n.
2. Configurar las credenciales para:
   - OpenAI
   - Gmail
   - Google Calendar
   - Clearbit
   - Calendly
3. Ajustar parámetros específicos en nodos `Set` y `Code` según estructura de datos y necesidades comerciales.
4. Verificar los triggers (`scheduleTrigger` y `calendlyTrigger`) según el flujo deseado.
5. Realizar pruebas iniciales para confirmar la integración completa.

## Detalles de funcionamiento
- **Investigación y generación de leads:** Utiliza OpenAI para enriquecer datos, Clearbit para información empresarial y nodos HTTP para consultas adicionales.
- **Filtrado y validación:** Nodos `filter`, `if` y `switch` determinan la calidad y el estado de los leads.
- **Gestión de agendas:** Integración con Calendly y Google Calendar para sincronizar citas y llamadas.
- **Comunicación:** Automatización de correos mediante Gmail con contenido personalizado generado por OpenAI y nodos HTML.
- **Control del flujo:** Uso de `merge`, `splitOut` y `noOp` para controlar el orden y manejo de datos en función de condiciones definidas.
- Total de nodos involucrados: 42, combinando lógica, comunicación y triggers.

## Ejemplos de uso
- **Ejemplo 1:** Automatizar la investigación y enriquecimiento de datos cuando un nuevo lead es creado en Calendly.
- **Ejemplo 2:** Enviar correos personalizados antes de la llamada para mejorar la tasa de conversión.
- **Ejemplo 3:** Sincronizar automáticamente citas en Google Calendar y validar la disponibilidad del equipo de ventas.
  
Este workflow es ideal para equipos de ventas que buscan optimizar la preparación y eficacia en llamadas de prospección mediante automatización e inteligencia artificial.
```
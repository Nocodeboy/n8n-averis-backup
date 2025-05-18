```markdown
# T - Lista de actividad en redes sociales de una empresa antes de una llamada copy

## Descripción

Workflow diseñado para recopilar y organizar la actividad en redes sociales de una empresa antes de realizar una llamada comercial o reunión. Facilita la preparación ofreciendo un resumen consolidado de interacciones y eventos relevantes, ayudando a personalizar la comunicación.

## Requisitos

- Credenciales de Gmail para enviar correos electrónicos.
- Acceso a Google Calendar.
- API Key de Clearbit para obtener información empresarial.
- Configuración de HTTP Request para acceder a fuentes externas de datos sociales.
- Permisos para utilizar nodos programados (Schedule Trigger).

## Instrucciones de configuración

1. **Gmail**: Configure sus credenciales OAuth2 en n8n para el nodo Gmail.
2. **Google Calendar**: Autorice acceso mediante las credenciales de Google.
3. **Clearbit**: Inserte su API Key en las credenciales correspondientes.
4. **HTTP Request**: Configure endpoints y parámetros para obtener datos de redes sociales.
5. Revise y ajuste horarios del nodo Schedule Trigger según la frecuencia deseada.
6. Personalice el filtro y lógica de nodos Switch y Filter conforme a sus criterios de negocio.

## Detalles de funcionamiento

- El trigger programado inicia el workflow en intervalos configurados.
- Obtiene información relevante desde APIs externas y bases de datos via HTTP Request y Clearbit.
- Procesa y filtra los datos mediante nodos Switch, Filter, y Code para adaptarlos al contexto.
- Combina información proveniente de diferentes fuentes con nodos Merge y SplitOut.
- Extrae y formatea contenido HTML para generar reportes o resúmenes.
- Envía correos a partir de la información procesada vía Gmail.
- Utiliza Google Calendar para verificar eventos o reuniones relacionadas.
- Añade notas y configuraciones internas con Set y StickyNote para facilitar seguimiento y trazabilidad.

## Ejemplos de uso

- Preparar un resumen quotidiano de actividad social antes de llamadas comerciales.
- Identificar eventos o menciones relevantes en redes sociales y calendarios.
- Automatizar el envío de informes resumidos a equipos de ventas o marketing.
- Enriquecer datos de contactos y empresas antes de interacciones clave.

---

**Categoría:** marketing/redes-sociales  
**Número de nodos:** 19  
**Nodos utilizados:** Switch, Merge, HTML, Filter, Code, Schedule Trigger, Gmail, Set, StickyNote, Clearbit, SplitOut, Google Calendar, HTTP Request  
**Etiquetas:** _(ninguna)_  
```
```markdown
# 3. Joe - Lead Scrapper Tool

## Descripción
Workflow diseñado para extraer y gestionar leads de manera automatizada, integrando múltiples fuentes y almacenando los datos en Google Sheets para facilitar su seguimiento y análisis.

## Requisitos
- Credenciales de Google Sheets configuradas en n8n.
- Acceso a las APIs necesarias para la recolección de datos (según finalidad del scrapper).
- n8n instalado y funcionando.

## Instrucciones de configuración
1. Importa el workflow en tu instancia de n8n.
2. Configura las credenciales de Google Sheets en la sección correspondiente.
3. Ajusta el nodo HTTP Request para apuntar a las fuentes de datos deseadas.
4. Personaliza los filtros y límites según la cantidad y tipo de leads que quieres procesar.
5. Verifica que los nombres de las hojas en Google Sheets coincidan con los configurados en el workflow.

## Detalles de funcionamiento
El workflow consta de 9 nodos que combinan diferentes funcionalidades:
- **Google Sheets**: Para lectura y escritura de datos.
- **Limit**: Controla la cantidad de registros procesados.
- **Filter**: Filtra los leads según criterios definidos.
- **Code**: Ejecuta lógica personalizada para procesar datos.
- **Execute Workflow Trigger**: Permite la ejecución condicional de flujos secundarios si es necesario.
- **Set**: Define y transforma variables internas.
- **HTTP Request**: Realiza llamadas a APIs externas para obtener información de leads.

## Ejemplos de uso
- Recolección diaria de leads desde plataformas externas.
- Filtrado automático de leads con criterios específicos (ej. ubicación, interés).
- Actualización y seguimiento en tiempo real de la base de datos de leads en Google Sheets.

---
Categoría: ventas/lead-generation  
Tipos de nodos utilizados: `googleSheets`, `limit`, `filter`, `code`, `executeWorkflowTrigger`, `set`, `httpRequest`  
Número de nodos: 9
```
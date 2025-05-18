```markdown
# T- Generea y enriquece leads con Apollo

## Descripción

Workflow de n8n diseñado para generar y enriquecer leads utilizando Apollo, integrando diversas fuentes de datos y automatizando su procesamiento para potenciar las ventas y la generación de leads.

## Requisitos

- Cuenta y credenciales de Apollo API.
- API key de OpenAI para el nodo `@n8n/n8n-nodes-langchain.openAi`.
- Acceso a Google Sheets con permisos para usar triggers y modificar hojas.
- Credenciales configuradas en n8n para Google Sheets.
- Acceso a Internet para llamadas HTTP externas.
- Configuración previa de credenciales en n8n para todos los nodos utilizados.

## Instrucciones de configuración

1. Importar el workflow en n8n.
2. Configurar las credenciales de Apollo API en `httpRequest`.
3. Añadir la API key de OpenAI en el nodo `openAi`.
4. Conectar y autorizar Google Sheets para triggers y edición.
5. Ajustar cualquier variable o parámetro en nodos `set` y `code` según necesidades específicas.
6. Revisar y personalizar el cron del `scheduleTrigger` para ejecución automática.

## Detalles de funcionamiento

- El workflow se activa principalmente mediante triggers de Google Sheets, formularios y programación.
- Utiliza Apollo para obtener datos de leads y enriquecerlos con información adicional.
- Procesa y filtra datos con nodos `if`, divide flujos con `splitOut` y transforma información con `code` y `set`.
- Aprovecha OpenAI para mejorar la calidad de los leads y dar contexto adicional.
- Se controla el flujo con notas adhesivas (`stickyNote`) para facilitar seguimiento.
- Ejecuta llamadas HTTP para integrar distintos endpoints y APIs externas.
- Los resultados se almacenan y actualizan en Google Sheets para acceso y análisis posteriores.

## Ejemplos de uso

- Generar automáticamente listas de leads cualificados basados en datos de formularios de contacto.
- Enriquecer listas existentes con información adicional proveniente de Apollo.
- Automatizar la actualización periódica de leads enriquecidos en Google Sheets.
- Filtrar y clasificar leads para campañas específicas usando lógica condicional integrada.

---

**Categoría:** ventas/lead-generation  
**Nodos utilizados:** @n8n/n8n-nodes-langchain.openAi, n8n-nodes-base.googleSheetsTrigger, n8n-nodes-base.googleSheets, n8n-nodes-base.if, n8n-nodes-base.formTrigger, n8n-nodes-base.code, n8n-nodes-base.scheduleTrigger, n8n-nodes-base.stickyNote, n8n-nodes-base.set, n8n-nodes-base.splitOut, n8n-nodes-base.httpRequest  
**Número de nodos:** 53  
**Etiquetas:** *(ninguna)*  
```
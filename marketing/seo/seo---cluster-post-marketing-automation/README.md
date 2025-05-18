```markdown
# SEO - Cluster Post

## Descripción
Workflow automatizado para la creación y gestión de contenidos SEO en clústeres de publicaciones, integrando Google Sheets, OpenAI y WordPress para optimizar estrategias de marketing digital.

## Requisitos
- Credenciales de Google Sheets con acceso a las hojas específicas.
- API Key de OpenAI (requerido para nodos Langchain - OpenAI).
- Acceso API a WordPress con permisos para crear y actualizar posts.
- Conexión a Internet para solicitudes HTTP externas.

## Instrucciones de configuración
1. Configure las credenciales de Google Sheets en n8n.
2. Añada su API Key de OpenAI en las credenciales correspondientes.
3. Establezca la conexión a WordPress con URL, usuario y contraseña o token.
4. Ajuste el nodo `scheduleTrigger` según la frecuencia deseada para ejecutar el workflow.
5. Modifique las hojas y endpoints HTTP según su entorno específico.

## Detalles de funcionamiento
- El workflow se inicia automáticamente según el trigger de programación configurado.
- Obtiene datos y keywords desde Google Sheets.
- Procesa y genera contenido SEO optimizado mediante OpenAI.
- Agrega y organiza la información con nodos de agregación y configuración interna.
- Realiza solicitudes HTTP externas para enriquecimiento o validación.
- Publica o actualiza los posts directamente en WordPress.
- Usa notas adhesivas (`stickyNote`) para recordatorios o información interna.
- Gestiona un total de 34 nodos integrados para un flujo completo y eficiente.

## Ejemplos de uso
- Automatizar la creación de clústeres de contenido SEO basados en keywords planificadas.
- Actualizar masivamente posts en WordPress con contenido generado automáticamente.
- Planificar y ejecutar campañas de marketing de contenidos con actualizaciones periódicas.
```
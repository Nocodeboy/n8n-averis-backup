```markdown
# Creación Automatizada de Contenido para Instagram a partir de Publicaciones en Tendencia

## Descripción
Workflow diseñado para automatizar la generación y publicación de contenido en Instagram, basado en análisis de publicaciones en tendencia. Utiliza inteligencia artificial para crear textos atractivos, gestiona la programación y publicación automática, optimizando la presencia en redes sociales.

## Requisitos
- Credenciales y acceso API para:
  - OpenAI (via @n8n/n8n-nodes-langchain.openAi)
  - Telegram (para notificaciones)
  - Facebook Graph API (para publicación en Instagram)
  - PostgreSQL (para almacenamiento y gestión de datos)
- n8n instalado y configurado
- Permisos adecuados para la gestión de cuentas de Instagram y Telegram

## Instrucciones de Configuración
1. **Configurar credenciales** en n8n para:
   - OpenAI API Key
   - Telegram Bot Token y chat ID
   - Facebook Graph API con permisos de Instagram Content Publishing
   - PostgreSQL base de datos con acceso para lectura y escritura
2. Ajustar nodo **Schedule Trigger** para determinar la frecuencia de ejecución.
3. Revisar y modificar las consultas en el nodo **Postgres** para adaptar a tus fuentes de datos.
4. Personalizar mensajes y formatos del contenido en los nodos de código y OpenAI.
5. Configurar nodos de publicación y notificación según tus necesidades específicas.

## Detalles de Funcionamiento
- El workflow inicia con un disparador programado.
- Obtiene datos relevantes de publicaciones en tendencia mediante consultas a PostgreSQL y peticiones HTTP.
- Utiliza OpenAI para generar textos optimizados para Instagram.
- Se aplican filtros y condiciones para asegurar la calidad y relevancia del contenido.
- El contenido se organiza y divide para una correcta publicación.
- Publica automáticamente en Instagram a través de la API de Facebook Graph.
- Envía notificaciones vía Telegram con el resumen del contenido publicado.
- Registra logs y datos relevantes para seguimiento y análisis.

## Ejemplos de Uso
- Publicar diariamente contenido personalizado basado en tendencias actuales.
- Notificar al equipo de marketing sobre nuevas publicaciones automáticamente.
- Ajustar fácilmente la programación para campañas específicas o eventos puntuales.

---

**Categoría:** marketing/redes-sociales  
**Nodos Utilizados:** @n8n/n8n-nodes-langchain.openAi, n8n-nodes-base.merge, n8n-nodes-base.if, n8n-nodes-base.code, n8n-nodes-base.telegram, n8n-nodes-base.scheduleTrigger, n8n-nodes-base.stickyNote, n8n-nodes-base.set, n8n-nodes-base.postgres, n8n-nodes-base.splitInBatches, n8n-nodes-base.httpRequest, n8n-nodes-base.facebookGraphApi  
**Número de nodos:** 44
```
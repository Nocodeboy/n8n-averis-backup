```markdown
# Promociona videos de Youtube en X

## Descripción
Workflow para automatizar la promoción de videos de YouTube en la plataforma X (antes Twitter), generando textos atractivos mediante OpenAI y publicándolos de forma programada.

## Requisitos
- Cuenta en YouTube con acceso a API Key (YouTube Data API v3).
- Cuenta en X (Twitter) con acceso a API Key, API Secret, Access Token y Access Token Secret.
- Cuenta en OpenAI con API Key para generar textos.
- n8n configurado con credenciales para YouTube, Twitter y OpenAI.

## Instrucciones de configuración
1. Agrega y configura las credenciales en n8n para:
    - YouTube (API Key).
    - Twitter/X (API Key, API Secret, Access Token, Access Token Secret).
    - OpenAI (API Key).
2. Ajusta el nodo `Schedule Trigger` para definir la frecuencia de promoción.
3. Configura el nodo `YouTube` para obtener los videos deseados (p. ej., últimos videos de un canal).
4. Verifica que el nodo de OpenAI esté preparado para generar textos promocionales usando los datos del video.
5. Configura el nodo `Twitter` para publicar los tweets generados.
6. Opcionalmente, utiliza nodos `Sticky Note` para anotaciones internas o seguimiento.

## Detalles de funcionamiento
- El workflow se activa según la programación del nodo `Schedule Trigger`.
- Obtiene los videos recientes de un canal de YouTube.
- Envía la información del video a OpenAI para generar una publicación atractiva.
- Publica el texto generado en X mediante el nodo dedicado.
- Utiliza nodos auxiliares para seguimiento y control interno.

## Ejemplos de uso
- Publicar automáticamente un tweet promocionando cada nuevo video publicado en YouTube.
- Automatizar la estrategia de marketing en redes sociales vinculada a contenido multimedia.
- Crear textos personalizados y atractivos con ayuda de inteligencia artificial para aumentar el alcance.

---

**Categoría:** marketing/redes-sociales  
**Nodos utilizados:** @n8n/n8n-nodes-langchain.openAi, n8n-nodes-base.twitter, n8n-nodes-base.scheduleTrigger, n8n-nodes-base.stickyNote, n8n-nodes-base.youTube  
**Número de nodos:** 6  
**Etiquetas:** _(ninguna)_  
```
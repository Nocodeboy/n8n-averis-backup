```markdown
# Crea post de Linkedin desde un RSS Feed

## Descripción  
Workflow diseñado para automatizar la creación y publicación de posts en LinkedIn a partir de contenidos extraídos de un RSS Feed. Utiliza procesamiento avanzado con OpenAI para generar textos atractivos y filtrar contenidos relevantes, optimizando la estrategia de marketing y contenido.

## Requisitos  
- Credenciales para LinkedIn (API de LinkedIn)  
- API Key de OpenAI para nodos LangChain (lmChatOpenAi, chainLlm, outputParserStructured)  
- Acceso a la fuente RSS configurada  
- Credenciales de Gmail (opcional, para notificaciones o envío de emails)  
- n8n instalado con los nodos mencionados  

## Instrucciones de configuración  
1. Configurar la fuente RSS en el nodo `rssFeedRead` con la URL del feed deseado.  
2. Ingresar las credenciales de LinkedIn en el nodo `linkedIn` para habilitar publicaciones.  
3. Añadir la API Key de OpenAI en los nodos `lmChatOpenAi`, `chainLlm` y `outputParserStructured`.  
4. Configurar el nodo `gmail` con tus credenciales si se requiere envío de notificaciones.  
5. Revisar y ajustar las reglas en nodos `if` y el procesamiento HTML según las necesidades de filtrado y formato.  
6. Guardar y activar el workflow.  

## Detalles de funcionamiento  
- El workflow inicia manualmente o por trigger automático, leyendo el RSS Feed configurado.  
- Se agregan y agregan datos para consolidar la información relevante (`aggregate`).  
- El contenido se procesa y analiza mediante nodos LangChain y OpenAI para generar textos optimizados para LinkedIn.  
- Se aplican filtros condicionales para seleccionar solo las noticias o artículos pertinentes.  
- Los posts son generados en formato HTML y publicados directamente en LinkedIn.  
- Opcionalmente, se envían notificaciones vía Gmail y se utilizan notas adhesivas (`stickyNote`) para seguimiento o comentarios internos.  
- Se manejan respuestas estructuradas y división de datos para asegurar precisión y orden en el flujo.  

## Ejemplos de uso  
- Publicar actualizaciones diarias sobre novedades de la industria a partir de un blog especializado.  
- Compartir artículos seleccionados automáticamente con resúmenes generados para captar la atención en LinkedIn.  
- Automatizar campañas de contenido para marketing, manteniendo presencia activa sin intervención manual constante.  

---

**Categoría:** marketing/contenido  
**Etiquetas:** Linkedin, Contenido, *****  
**Número de nodos:** 29  
```
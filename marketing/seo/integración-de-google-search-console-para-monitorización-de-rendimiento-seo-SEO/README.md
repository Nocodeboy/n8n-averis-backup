```markdown
# Integración de Google Search Console para Monitorización de Rendimiento SEO

## Descripción
Workflow diseñado para extraer y monitorizar datos de rendimiento SEO desde Google Search Console, facilitando el análisis automatizado y seguimiento continuo de métricas clave para optimizar estrategias de marketing digital.

## Requisitos
- Cuenta activa de Google con acceso a Google Search Console.
- Credenciales de API para Google Search Console configuradas en n8n.
- n8n con nodos base necesarios: Manual Trigger, Code, HTTP Request, Sticky Note.

## Instrucciones de configuración
1. Configure las credenciales de Google Search Console en n8n (OAuth2).
2. Importe o cree el workflow asegurándose de incluir los 7 nodos.
3. Modifique el nodo `HTTP Request` con los parámetros específicos de su propiedad en Search Console.
4. Ajuste el nodo `Code` para procesar las respuestas según los datos requeridos.
5. Utilice el `Manual Trigger` para iniciar manualmente o integre con triggers externos según su flujo.

## Detalles de funcionamiento
- El workflow inicia con un trigger manual.
- El nodo `HTTP Request` realiza consultas a la API de Google Search Console para obtener métricas de rendimiento.
- El nodo `Code` procesa y formatea los datos recibidos.
- Se utilizan nodos de nota adhesiva (`Sticky Note`) para incluir instrucciones o comentarios dentro del flujo.
- Permite la monitorización periódica y análisis de datos SEO para ajustar estrategias rápidamente.

## Ejemplos de uso
- Extraer clics, impresiones y posición media de búsquedas orgánicas de un sitio web.
- Generar informes automatizados de rendimiento SEO para equipos de marketing.
- Detectar anomalías en el tráfico orgánico mediante la supervisión continua de métricas clave.

---

**Categoría:** marketing/seo  
**Etiquetas:** SEO  
**Nodos:** 7 (Manual Trigger, Code, HTTP Request, Sticky Note)
```
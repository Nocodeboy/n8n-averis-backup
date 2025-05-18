```markdown
# Análisis SEO Semanal con IA desde Google Analytics y Search Console a Baserow

## Descripción  
Workflow para realizar un análisis SEO semanal combinando datos de Google Analytics y Google Search Console, procesándolos con IA y almacenando los resultados en Baserow para facilitar la monitorización y toma de decisiones.

## Requisitos  
- Credenciales de Google Analytics con acceso a la propiedad correspondiente.  
- Credenciales de Google Search Console con acceso al sitio web a analizar.  
- Cuenta y API Token de Baserow para conexión y escritura de datos.  
- n8n configurado con acceso a los siguientes nodos:  
  - `n8n-nodes-base.baserow`  
  - `n8n-nodes-base.manualTrigger`  
  - `n8n-nodes-base.code`  
  - `n8n-nodes-base.googleAnalytics`  
  - `n8n-nodes-base.scheduleTrigger`  
  - `n8n-nodes-base.stickyNote`  
  - `n8n-nodes-base.httpRequest`

## Instrucciones de configuración  
1. Configurar las credenciales de Google Analytics y Search Console en n8n.  
2. Añadir la API Token y URL base de Baserow en las credenciales correspondientes.  
3. Ajustar el nodo `scheduleTrigger` para definir la frecuencia semanal deseada.  
4. Revisar y adaptar el nodo `code` en caso de modificaciones o personalizaciones en el procesamiento de datos.  
5. Verificar las tablas y columnas en Baserow para asegurar compatibilidad con el esquema de salida.

## Detalles de funcionamiento  
- El workflow se activa semanalmente vía `scheduleTrigger`.  
- Extrae datos relevantes de SEO desde Google Analytics y Search Console.  
- Los datos se procesan mediante nodos de código y llamadas HTTP para aplicar análisis con IA (posiblemente mediante una API externa).  
- Finalmente, los resultados se almacenan en Baserow para su consulta y seguimiento.  
- Incluye nodos manuales y sticky notes para gestión interna y control de ejecución.

## Ejemplos de uso  
- Monitorizar semanalmente el rendimiento SEO y las tendencias de tráfico orgánico.  
- Detectar oportunidades de mejora en keywords y contenido web automáticamente.  
- Compartir informes y métricas actualizadas con el equipo marketing mediante Baserow.  
- Automatizar workflows de análisis SEO para ganar eficiencia y precisión.

---

**Número de nodos:** 22  
**Categoría:** marketing/seo  
**Etiquetas:** _(ninguna asignada)_
```
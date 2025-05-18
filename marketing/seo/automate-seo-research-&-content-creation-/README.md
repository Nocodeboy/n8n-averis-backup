```markdown
# Automate SEO Research & Content Creation

## Descripción
Este workflow de n8n automatiza tareas clave de investigación SEO y creación de contenido, integrando múltiples nodos para recopilar datos, analizar tendencias y generar textos optimizados de forma eficiente.

## Requisitos
- Credenciales de OpenAI (para nodos `lmChatOpenAi`, `openAi` y `agent`)
- Credenciales de Google Sheets (para almacenar y leer datos)
- Acceso a APIs externas según configuración (utilizadas por `httpRequest` y `xml` nodes)
- n8n con soporte para nodos de Langchain y nodos base estándar

## Instrucciones de configuración
1. Configure las credenciales de OpenAI en n8n.
2. Configure las credenciales de Google Sheets con acceso a las hojas requeridas.
3. Revise y personalice los endpoints y parámetros en los nodos `httpRequest` y `xml` según sus fuentes de datos SEO.
4. Ajuste los triggers (`manualTrigger` o `scheduleTrigger`) para definir la frecuencia de ejecución.
5. Verifique que los nodos de límite (`limit`) y agregación (`aggregate`) estén correctamente configurados para manejar el volumen de datos esperado.

## Detalles de funcionamiento
- El workflow inicia mediante un disparador manual o programado.
- Consulta datos SEO externos a través de nodos `httpRequest` y procesamiento XML.
- Utiliza nodos Langchain para analizar la información y generar contenido optimizado vía OpenAI.
- Almacena resultados en Google Sheets para seguimiento y futuras referencias.
- Aplica nodos de agregación y límite para controlar el flujo y volumen de datos.
- Incluye nodos `set` y `stickyNote` para gestión interna y anotaciones durante el proceso.
  
**Número total de nodos:** 24  
**Tipos de nodos involucrados:**  
`aggregate`, `lmChatOpenAi`, `limit`, `googleSheets`, `openAi`, `manualTrigger`, `scheduleTrigger`, `stickyNote`, `set`, `agent`, `xml`, `splitOut`, `httpRequest`

## Ejemplos de uso
- Generar semanalmente un informe de palabras clave y contenido optimizado para nuevas campañas SEO.  
- Automatizar la creación de borradores de artículos basados en tendencias detectadas en múltiples fuentes.  
- Monitorizar términos específicos y actualizar hojas de cálculo con recomendaciones automatizadas.  
- Integrar con Google Sheets para facilitar la colaboración y revisión de contenidos antes de su publicación.

---
*Categoría: marketing/seo*
```
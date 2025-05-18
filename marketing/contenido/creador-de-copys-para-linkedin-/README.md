```markdown
# Creador de Copys para Linkedin

## Descripción
Workflow de n8n que automatiza la creación de copys atractivos para publicaciones en LinkedIn, combinando datos desde Google Sheets con inteligencia artificial para generar textos personalizados y efectivos.

## Requisitos
- Credenciales de Google Sheets para acceso y lectura de hojas de cálculo.
- API Key del servicio OpenRouter para el nodo `lmChatOpenRouter`.
- Configuración del agente Langchain para procesamiento de lenguaje natural.
- Acceso a internet para realizar peticiones HTTP mediante el nodo `httpRequest`.
- n8n versión compatible con los nodos utilizados.

## Instrucciones de configuración
1. Configura la credencial de Google Sheets en n8n con acceso a la hoja que contiene los datos para los copys.
2. Proporciona tu API Key de OpenRouter en el nodo `lmChatOpenRouter`.
3. Ajusta los parámetros del agente Langchain (`@n8n/n8n-nodes-langchain.agent`) según las necesidades de tu flujo de contenido.
4. Verifica que el nodo `httpRequest` esté configurado correctamente para cualquier llamada externa que requiera el workflow.
5. Activa el nodo `manualTrigger` para iniciar manualmente la ejecución del workflow.

## Detalles de funcionamiento
El workflow consta de 6 nodos que permiten:
- Activar el proceso manualmente.
- Leer datos desde Google Sheets.
- Procesar y generar textos mediante un agente Langchain que utiliza OpenRouter.
- Realizar llamadas HTTP para obtener información adicional o enviar resultados.
- Generar copys personalizados para LinkedIn basados en los datos proporcionados.

## Ejemplos de uso
- Generar copys semanales para publicaciones de marketing en LinkedIn utilizando datos actualizados en una hoja de Google Sheets.
- Crear mensajes personalizados para distintos públicos objetivo, ajustando el prompt del agente Langchain.
- Integrar con otras APIs vía HTTP para enriquecer el contenido generado antes de publicarlo.

---
**Número de nodos:** 6  
**Categoría:** marketing/contenido  
**Etiquetas:** *(ninguna definida)*
```
```markdown
# Creación de videos Faceless para Youtube

## Descripción
Workflow automatizado para la creación de videos faceless (sin aparecer en cámara) para Youtube, que integra generación de contenido, gestión de datos en Google Sheets, procesamiento con modelos de lenguaje y publicación directa en Youtube.

## Requisitos
- Cuenta de Google con acceso a Google Sheets y Youtube Data API.
- Credenciales configuradas para:
  - Google Sheets
  - Youtube
- Acceso a servicios de LangChain con el nodo `lmChatOpenRouter` y agentes compatibles.
- n8n configurado con los nodos mencionados y permisos adecuados.

## Instrucciones de configuración
1. **Credenciales**
   - Añade tus credenciales de Google Sheets y Youtube en n8n.
   - Configura la API key o token para OpenRouter y agentes de LangChain.
2. **Google Sheets**
   - Crea o vincula una hoja de cálculo que almacene los datos para contenidos y guiones.
3. **LangChain**
   - Ajusta los parámetros del nodo `lmChatOpenRouter` y agentes según tus prompts y objetivos.
4. **Programación**
   - Configura el nodo `scheduleTrigger` para definir la frecuencia de creación y publicación.
5. **Parámetros del workflow**
   - Revisa y adapta nodos de configuración como `switch`, `splitInBatches` y `wait` para optimizar flujo.

## Detalles de funcionamiento
- El workflow inicia con un trigger manual o programado.
- Lee y gestiona datos desde Google Sheets para contenido y guiones.
- Utiliza LangChain para generación, refinamiento y estructura del texto.
- Divide las tareas en batches para procesamiento escalable.
- Realiza llamadas HTTP para integrar con servicios externos si es necesario.
- Almacena notas y datos intermedios mediante el nodo `stickyNote`.
- Finalmente, sube y publica el video en Youtube usando el nodo dedicado.
- Incluye manejo de esperas y condiciones con nodos `wait` y `switch`.
- Total de nodos en el flujo: 32.

## Ejemplos de uso
- Automatizar la creación de videos educativos sin necesidad de grabación personal.
- Generar contenido de marketing visual para canales de Youtube de forma periódica.
- Integrar generación de guiones y publicación en un solo proceso automatizado.

---
*Categoría: marketing/contenido*  
*Número de nodos: 32*  
*Etiquetas: (sin etiquetas asignadas)*
```
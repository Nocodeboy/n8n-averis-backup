```markdown
# Automatizar Copy Redes Sociales

## Descripción

Workflow diseñado para automatizar la generación de copies para redes sociales, integrando inteligencia artificial y gestión de datos en Google Sheets para optimizar la creación y publicación de contenido de marketing.

## Requisitos

- Cuenta y credenciales de OpenAI para el nodo `@n8n/n8n-nodes-langchain.openAi`.
- Acceso a Google Sheets con las credenciales adecuadas para lectura y escritura.
- n8n instalado y configurado para ejecutar workflows.
- Permisos para ejecutar nodos HTTP Request y Code.

## Instrucciones de configuración

1. **Configurar credenciales:**
   - Agregar las credenciales de OpenAI en n8n.
   - Añadir credenciales de Google Sheets con acceso a la hoja correspondiente.

2. **Ajustar nodos:**
   - Revisar y actualizar URLs, IDs de hojas y parámetros en nodos Google Sheets y HTTP Request según el proyecto.
   - Adaptar los prompts de OpenAI en función del tipo de contenido a generar.

3. **Activar manualTrigger:**
   - El workflow inicia con un nodo `manualTrigger` para iniciar la automatización cuando se requiera.

## Detalles de funcionamiento

- **Inicio:** Se activa manualmente o mediante trigger externo.
- **Generación de contenido:** Utiliza OpenAI para crear copies con base en datos obtenidos.
- **Evaluación condicional:** Nodos `switch` e `if` filtran y direccionan el flujo según criterios definidos.
- **Gestión de datos:** Información leída y actualizada en Google Sheets para control y seguimiento.
- **Procesamiento avanzado:** Nodo `code` especializado para manipulaciones personalizadas.
- **Integraciones HTTP:** Solicitudes externas para enriquecer o validar datos si es necesario.
- Total de nodos: 20, distribuidos para asegurar eficiencia y claridad en el flujo.

## Ejemplos de uso

- Generar automáticamente copies para campañas específicas en Instagram y Facebook.
- Actualizar bases de datos de contenido con nuevos textos creados por IA.
- Filtrar y segmentar copies según tipo de público mediante nodos condicionales.
- Ejecutar la generación y publicación desde un disparador manual para control total.

---
**Etiquetas:** Redes Sociales, Contenido  
**Categoría:** marketing/contenido
```

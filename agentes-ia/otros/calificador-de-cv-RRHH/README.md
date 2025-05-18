```markdown
# Calificador de CV

## Descripción
Workflow diseñado para automatizar la evaluación y calificación de currículums vitae (CV) utilizando inteligencia artificial. Permite extraer información de los CVs, clasificarlos y almacenar los resultados para facilitar los procesos de selección en RRHH.

## Requisitos
- Credenciales de Airtable para almacenamiento de datos.
- API Key de OpenAI para los nodos de Langchain (lmChatOpenAi, chainLlm, textClassifier).
- Configuración de acceso a los archivos de CV (puede ser a través de HTTP o carga directa).
- n8n versión compatible con los nodos utilizados.

## Instrucciones de configuración
1. Configure las credenciales de Airtable en n8n con la base y tabla adecuadas para almacenar resultados.
2. Añada la API Key de OpenAI en las credenciales de Langchain.
3. Ajuste el nodo `formTrigger` para iniciar el proceso con la entrada requerida (formularios u otro trigger).
4. Verifique la correcta conexión de nodos para extracción (`extractFromFile`) y clasificación (`textClassifier`).
5. Configure endpoints o rutas HTTP si se usa el nodo `httpRequest` para obtener archivos externos.
6. Personalice los parámetros de análisis según necesidad en los nodos de Langchain.

## Detalles de funcionamiento
- El workflow se inicia mediante un formulario o trigger configurado.
- Los archivos de CV se extraen y procesan para obtener texto utilizable.
- La IA, mediante nodos Langchain, analiza y clasifica los CV según parámetros predefinidos.
- Los resultados estructurados se almacenan en Airtable para seguimiento y análisis.
- Notas y comentarios se pueden añadir con los nodos `stickyNote`.
- Se puede usar `httpRequest` para integrar fuentes externas o APIs adicionales.

## Ejemplos de uso
- Evaluación automática de candidatos recibidos vía formulario web.
- Clasificación de CVs según experiencia, habilidades o requisitos específicos.
- Generación de reportes estructurados para selección de personal.
- Integración con sistemas internos mediante HTTP para alimentar bases de datos de RRHH.

---

**Categoría:** agentes-ia/otros  
**Nodos utilizados (23):**  
n8n-nodes-base.form, @n8n/n8n-nodes-langchain.lmChatOpenAi, @n8n/n8n-nodes-langchain.chainLlm, n8n-nodes-base.formTrigger, n8n-nodes-base.extractFromFile, n8n-nodes-base.stickyNote, n8n-nodes-base.airtable, @n8n/n8n-nodes-langchain.outputParserStructured, n8n-nodes-base.httpRequest, @n8n/n8n-nodes-langchain.textClassifier  
**Etiquetas:** RRHH
```
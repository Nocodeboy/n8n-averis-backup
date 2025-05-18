```markdown
# Sistema Multiagentes Investigación profunda

## Descripción
Workflow diseñado para implementar un sistema multiagentes basado en agentes inteligentes y Recuperación Augmentada por Generación (RAG), que facilita procesos avanzados de investigación profunda mediante integración de múltiples nodos y tecnologías.

## Requisitos
- Credenciales de Google Sheets para acceso y manipulación de hojas de cálculo.
- API key válida para OpenRouter (modelos de lenguaje de Langchain).
- Acceso a endpoints HTTP necesarios según configuración.
- n8n versión compatible con nodos de Langchain (`@n8n/n8n-nodes-langchain`).

## Instrucciones de configuración
1. Configure y autentique la credencial de Google Sheets en n8n.
2. Añada la API key de OpenRouter en las credenciales correspondientes.
3. Revise y ajuste las URLs y parámetros en nodos `httpRequest` según su entorno.
4. Active el trigger de formulario (`formTrigger`) para iniciar el workflow según su necesidad.
5. Valide los ajustes en nodos `set`, `code` y `switch` para personalización de lógica.

## Detalles de funcionamiento
Este workflow cuenta con 89 nodos que combinan funcionalidades para:  
- Captura y procesamiento de datos vía formularios.  
- Consulta y agregación de datos en Google Sheets.  
- División y combinación de flujos con nodos `splitOut`, `merge` y `limit`.  
- Comunicación con agentes Langchain para generación de respuestas inteligentes.  
- Análisis y filtrado dinámico con nodos `switch` y `code`.  
- Presentación de resultados mediante nodos HTML y notas adhesivas (`stickyNote`).  
- Interpretación estructurada de salidas mediante `outputParserStructured`.

## Ejemplos de uso
- Implementar un sistema de investigación que recupere y analice información almacenada en Google Sheets y genere respuestas detalladas con agentes IA.  
- Automatizar la revisión y filtrado de datos para homenajear insights clave con agentes especializados.  
- Crear flujos interactivos que combinan inputs de usuarios con procesamiento avanzado y generación de contenido dinámico.

---

**Etiquetas:** Averis, Multiagentes, Investigación  
**Categoría:** agentes-ia/rag  
**Tipos de nodos:** googleSheets, aggregate, switch, limit, merge, lmChatOpenRouter, html, formTrigger, code, agent, stickyNote, set, outputParserStructured, splitOut, httpRequest  
**Número de nodos:** 89
```
```markdown
# Clasificador de emails - daniel@averis.es

## Descripción
Workflow diseñado para clasificar automáticamente emails utilizando modelos de lenguaje avanzados a través de nodos de LangChain y Gmail en n8n. Facilita la organización y gestión de correos entrantes en base a categorías definidas.

## Requisitos
- Cuenta de Gmail con acceso IMAP habilitado.
- Credenciales OAuth2 configuradas en n8n para nodos Gmail.
- API key válida para OpenAI (usada por el nodo `lmChatOpenAi`).
- n8n instalado con los paquetes:
  - `@n8n/n8n-nodes-langchain`
  - `n8n-nodes-base`

## Configuración
1. Configure las credenciales de Gmail en n8n para acceso al correo.
2. Configure la API key de OpenAI en la sección de credenciales para LangChain.
3. Importe el workflow en n8n.
4. Ajuste los parámetros de clasificación según sus necesidades en el nodo `textClassifier`.
5. Active el workflow para que escuche nuevos emails mediante el nodo `gmailTrigger`.

## Funcionamiento
- El nodo `gmailTrigger` detecta nuevos emails.
- Los mensajes pasan por filtros y preprocesamiento.
- El nodo `lmChatOpenAi` procesa el contenido del email para contextualizar.
- El nodo `textClassifier` evalúa y clasifica el email en categorías predefinidas.
- Dependiendo de la clasificación, se pueden disparar acciones automáticas (respuestas, etiquetas, redirecciones).
- Puede ejecutarse manualmente con el nodo `manualTrigger` para pruebas o clasificación puntual.

## Ejemplos de uso
- Clasificación automática de emails de soporte por tipo de consulta.
- Identificación y etiquetado de correos prioritarios o relacionados con proyectos específicos.
- Automatización de respuestas iniciales basadas en la categoría del email.

---

**Categoría:** utilidades/otros  
**Etiquetas:** Averis, Email  
**Nodos en total:** 12 (`@n8n/n8n-nodes-langchain.lmChatOpenAi`, `n8n-nodes-base.gmailTrigger`, `n8n-nodes-base.manualTrigger`, `n8n-nodes-base.gmail`, `@n8n/n8n-nodes-langchain.textClassifier`)
```
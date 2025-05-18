```markdown
# Extrae datos de matricula

## Descripción
Workflow diseñado para extraer y procesar datos de matrícula utilizando inteligencia artificial. Automatiza la captura y análisis de información relevante a partir de formularios.

## Requisitos
- Credenciales de OpenRouter API para el nodo `lmChatOpenRouter`.
- Acceso a n8n con los nodos instalados:
  - `n8n-nodes-base.form`
  - `@n8n/n8n-nodes-langchain.lmChatOpenRouter`
  - `@n8n/n8n-nodes-langchain.chainLlm`
  - `n8n-nodes-base.formTrigger`
  - `n8n-nodes-base.set`

## Instrucciones de configuración
1. Configurar las credenciales de OpenRouter en n8n.
2. Ajustar el formulario en el nodo `form` según los campos requeridos para la matrícula.
3. Verificar y ajustar las cadenas de procesamiento en `chainLlm` para adecuarse a los datos específicos.
4. Configurar el nodo `formTrigger` para iniciar el workflow al recibir datos.
5. Personalizar el nodo `set` para definir las salidas o formatos deseados.

## Detalles de funcionamiento
- El workflow se inicia mediante el nodo `formTrigger` al recibir un formulario de matrícula.
- El nodo `form` recoge los datos ingresados por el usuario.
- El nodo `lmChatOpenRouter` utiliza inteligencia artificial para interpretar y validar la información.
- `chainLlm` procesa la salida del modelo para extraer los datos estructurados.
- Finalmente, el nodo `set` organiza y prepara los datos para su uso posterior o exportación.

## Ejemplos de uso
- Automatización en centros educativos para el ingreso de datos de matrícula de estudiantes.
- Agilización de procesos administrativos mediante extracción rápida y fiable de información.
- Integración con otros sistemas para la validación automática de registros.

---

**Categoría:** agentes-ia/otros  
**Número de nodos:** 5  
**Etiquetas:** _(No aplican)_
```
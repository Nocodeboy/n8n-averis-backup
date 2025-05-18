```markdown
# Gestión de emails

## Descripción
Workflow diseñado para optimizar la gestión de correos electrónicos mediante la integración de OpenAI (modelos de lenguaje y embeddings), Gmail, Telegram y herramientas de memoria y vectorización. Facilita la lectura, clasificación, respuesta automática y seguimiento eficiente de emails.

## Requisitos
- Credenciales de Gmail API para acceder y gestionar correos.
- API key de OpenAI para nodos de lenguaje y embeddings (`lmChatOpenAi` y `embeddingsOpenAi`).
- Cuenta y credenciales Supabase para el vector store (`vectorStoreSupabase`).
- Token de Telegram para enviar y recibir notificaciones.
- Acceso a n8n con los nodos mencionados instalados y habilitados.

## Instrucciones de configuración
1. Configure las credenciales de Gmail, OpenAI, Supabase y Telegram en n8n.
2. Importe el workflow en su instancia de n8n.
3. Ajuste parámetros específicos (como filtros de emails, triggers, o mensajes de respuesta) según sus necesidades.
4. Habilite el workflow y pruebe con emails reales para validar la integración.

## Detalles de funcionamiento
- Utiliza nodos de OpenAI para analizar y generar respuestas personalizadas a emails.
- Emplea embeddings y vector store Supabase para almacenar y recuperar contexto e información relevante.
- La lógica condicional (`switch`, `if`) clasifica y determina acciones para diferentes tipos de correos.
- Envía notificaciones y alertas vía Telegram para tareas críticas o seguimiento.
- Incluye memoria de ventana y agentes para mantener contexto conversacional y ejecutar tareas complejas.
- Realiza peticiones HTTP para complementar integraciones externas cuando es necesario.
- Cuenta con 42 nodos organizados para garantizar un flujo eficiente y modular.

## Ejemplos de uso
- Automatizar respuestas a consultas frecuentes recibidas por Gmail.
- Clasificar y priorizar emails importantes usando análisis de lenguaje natural.
- Enviar alertas vía Telegram para correos con asuntos críticos.
- Mantener un historial incrustado en vector store Supabase para referencias rápidas y búsqueda semántica.

---
*Categoría:* productividad/tareas  
*Número de nodos:* 42  
*Etiquetas:* (ninguna definida)  
```
```markdown
# Verificación Automatizada de Pagos de Alquiler con IA a partir de Extractos Bancarios

## Descripción
Workflow diseñado para automatizar la verificación de pagos de alquiler mediante el análisis inteligente de extractos bancarios. Utiliza IA para extraer información relevante y validar el cumplimiento de pagos, facilitando el seguimiento en el área de ventas y administración.

## Requisitos
- Credenciales de acceso a OpenAI para nodos de lenguaje (@n8n/n8n-nodes-langchain.lmChatOpenAi)
- Permisos para lectura y escritura de archivos en el entorno local
- Acceso al directorio donde se recibirán los extractos bancarios
- n8n v1.0 o superior compatible con los nodos LangChain integrados

## Instrucciones de configuración
1. Configure las credenciales de OpenAI en n8n.
2. Establezca la carpeta de monitoreo para el nodo `localFileTrigger` con los extractos bancarios en formato compatible.
3. Ajuste las propiedades de los nodos de extracción para el formato específico de sus archivos.
4. Verifique las rutas para lectura y escritura de archivos locales en los nodos correspondientes.
5. Personalice los parámetros del agente y parseadores de salida según necesite para el análisis y reporte.

## Detalles de funcionamiento
1. El workflow se activa con la llegada de un nuevo extracto bancario (nodo `localFileTrigger`).
2. El archivo es leído y procesado por el nodo `extractFromFile`.
3. La IA analiza el contenido mediante `lmChatOpenAi` junto con herramientas de código para interpretar y validar los datos (nodos `toolCode`, `code`).
4. La información estructurada es parseada con `outputParserStructured`.
5. Se generan notas y reportes automáticos para seguimiento (nodos `stickyNote`, `set`).
6. Los datos pueden dividirse y manipularse con `splitOut` y guardarse localmente para referencias futuras.

## Ejemplos de uso
- Verificar automáticamente si los pagos de alquiler correspondientes a un período determinado fueron recibidos correctamente.
- Generar alertas y reportes sobre pagos pendientes o inconsistencias detectadas en extractos bancarios.
- Integrar con sistemas de CRM para actualizar el estado de cuentas y facilitar la gestión comercial.

---
*Workflow con 18 nodos que integra capacidades avanzadas de IA para optimizar el seguimiento de ventas y cobranzas.*
```
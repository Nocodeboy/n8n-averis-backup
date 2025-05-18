```markdown
# 4. Joe - Email Preparation Tool

## Descripción
Workflow diseñado para facilitar la preparación y personalización de campañas de email marketing, integrando Google Sheets para la gestión de datos y OpenAI para la generación de contenido.

## Requisitos
- Credenciales de Google Sheets con acceso a la hoja de cálculo correspondiente.
- API Key de OpenAI para el nodo Langchain.
- Acceso a internet para nodos HTTP Request.
- Configuración de credenciales en n8n para cada nodo utilizado.

## Instrucciones de configuración
1. Configure las credenciales de Google Sheets en n8n.
2. Agregue su API Key de OpenAI en el nodo correspondiente.
3. Ajuste los parámetros en el nodo de Schedule Trigger para definir la frecuencia de ejecución.
4. Actualice las URLs o endpoints en los nodos HTTP Request según su flujo de trabajo.
5. Personalice las hojas y rangos de Google Sheets con los datos de sus campañas.

## Detalles de funcionamiento
- El workflow inicia automáticamente según la programación establecida.
- Extrae datos desde Google Sheets para obtener información de los destinatarios.
- Utiliza OpenAI para generar o adaptar contenidos de email.
- Incluye nodos limit y merge para controlar el flujo y combinar datos.
- Ejecuta scripts personalizados con nodos code para transformaciones específicas.
- Envía solicitudes HTTP para integrar con servicios externos si es necesario.
- Finalmente, prepara y almacena los emails listos para envío o revisión.

## Ejemplos de uso
- Generación automática de texto personalizado para campañas de email.
- Extracción y actualización masiva de datos de clientes desde Google Sheets.
- Integración con servicios externos para validación o seguimiento de emails.
```
# Agentes de IA para WhatsApp

Esta carpeta contiene workflows de n8n para implementar agentes de IA en WhatsApp.

## Workflows disponibles

- **1-main-agent-agente-ia-avanzado-whatsapp**: El workflow principal que gestiona la integración con WhatsApp
- **2-interno-clinica**: Workflow auxiliar para la gestión interna de clínicas
- **3-recordatorio-citas**: Automatización de recordatorios de citas para pacientes

## Configuración necesaria

1. **API de WhatsApp**: Necesitas una cuenta en WhatsApp Business API o un proveedor compatible
2. **Credenciales de IA**: Claves API para los modelos de IA utilizados (OpenAI, Claude, etc.)
3. **Webhooks**: Configuración de las URLs de webhook en tu proveedor de WhatsApp

## Guía de implementación

1. Importa primero el workflow principal
2. Configura las variables de entorno necesarias
3. Añade las credenciales de WhatsApp y los servicios de IA
4. Implementa los workflows auxiliares según tus necesidades
5. Prueba la integración con mensajes de prueba

## Resolución de problemas comunes

- **Error de webhook**: Verifica que la URL del webhook sea accesible públicamente
- **Tiempos de respuesta**: Ajusta los timeouts en caso de respuestas lentas del modelo de IA
- **Límites de API**: Ten en cuenta los límites de las APIs de WhatsApp y los servicios de IA

## Ejemplos de uso

Incluye ejemplos específicos de mensajes que se pueden enviar al chatbot y las respuestas esperadas.

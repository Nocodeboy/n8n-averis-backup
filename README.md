# n8n-averis-backup

Repositorio de backup y documentación para workflows de n8n de Averis.

## Estructura del repositorio

El repositorio está organizado por categorías funcionales:

- **agentes-ia/**: Workflows relacionados con agentes de IA (WhatsApp, Telegram, etc.)
  - **whatsapp/**: Agentes específicos para WhatsApp
  - **telegram/**: Agentes específicos para Telegram
  - **ecommerce/**: Agentes especializados en ecommerce
  - **clinica-dental/**: Agentes para clínicas dentales
  - **rag/**: Sistemas RAG (Retrieval Augmented Generation)

- **marketing/**: Workflows para marketing digital
  - **contenido/**: Generación y gestión de contenido
  - **redes-sociales/**: Automatizaciones para redes sociales
  - **seo/**: Herramientas para SEO
  - **email/**: Campañas de email marketing

- **ventas/**: Workflows de ventas y CRM
  - **lead-generation/**: Generación y cualificación de leads
  - **cotizaciones/**: Gestión de cotizaciones
  - **seguimiento/**: Seguimiento de clientes potenciales

- **productividad/**: Herramientas de productividad interna
  - **agenda/**: Gestión de calendario y citas
  - **reuniones/**: Organización y seguimiento de reuniones
  - **tareas/**: Gestión de tareas

- **utilidades/**: Herramientas generales y utilidades
  - **backup/**: Scripts de backup
  - **scraping/**: Herramientas de web scraping
  - **integraciones/**: Integraciones con otros servicios

## Instrucciones de uso

1. Navega a la carpeta correspondiente al tipo de workflow que necesitas
2. Cada workflow tiene su propio README con instrucciones específicas
3. Los archivos JSON pueden importarse directamente en n8n

## Nomenclatura de archivos

El formato de nomenclatura recomendado es:
```
[número]-[nombre-descriptivo]-[versión/variante]-[plataforma].json
```

Ejemplo: `1-agente-ia-ecommerce-rag-v2-whatsapp.json`

## Cómo contribuir

1. Utiliza la estructura de carpetas existente
2. Añade documentación detallada a los READMEs
3. Mantén un formato consistente en los nombres de los archivos
4. Actualiza la documentación cuando modifiques workflows existentes

## Recursos adicionales

- [Documentación oficial de n8n](https://docs.n8n.io/)
- [Guía interna de Averis para n8n](https://docs.averis.es/n8n-guide)

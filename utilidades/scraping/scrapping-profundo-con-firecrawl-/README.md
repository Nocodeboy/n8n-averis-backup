```markdown
# Scrapping Profundo con FireCrawl

## Descripción
Este workflow de n8n permite realizar scrapping profundo utilizando FireCrawl, facilitando la extracción automatizada de datos web con control de flujo y tiempos de espera para optimizar el proceso.

## Requisitos
- n8n versión compatible con los nodos usados.
- Conexión a internet para realizar solicitudes HTTP.
- API o endpoints accesibles y permitidos para scrapping.
- (Opcional) Credenciales API si los endpoints lo requieren.

## Instrucciones de configuración
1. Importa el workflow en tu instancia de n8n.
2. Si es necesario, configura las credenciales para las solicitudes HTTP en el nodo `httpRequest`.
3. Ajusta parámetros en los nodos `set` para definir URLs, filtros o tiempos de espera según tu caso.
4. Revisa y personaliza las condiciones en el nodo `if` para controlar el flujo lógico.
5. Guarda y activa el workflow.

## Detalles de funcionamiento
- El workflow inicia manualmente con el nodo `manualTrigger`.
- Utiliza nodos `set` para preparar datos y parámetros.
- El nodo `httpRequest` realiza las solicitudes para el scrapping.
- El nodo `wait` regula los tiempos entre solicitudes para evitar bloqueos.
- El nodo `if` determina rutas según condiciones específicas.
- `stickyNote` sirve para anotaciones internas y organización.
- En total, el workflow consta de 9 nodos que combinan estas funcionalidades para un scrapping profundo y controlado.

## Ejemplos de uso
- Extraer datos detallados de catálogos de productos en múltiples páginas.
- Recolectar información estructurada de sitios web que requieren navegación paso a paso.
- Automatizar la recopilación de contenidos dinámicos con pausas entre solicitudes.

---
**Categoría:** utilidades/scraping  
**Nodos utilizados:** `if`, `manualTrigger`, `stickyNote`, `set`, `httpRequest`, `wait`  
**Número total de nodos:** 9
```
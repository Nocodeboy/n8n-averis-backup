```markdown
# 7. Agente para Abogados - Error

## Descripción
Este workflow está diseñado para detectar y manejar errores en procesos relacionados con agentes para abogados, utilizando un disparador de error y enviando notificaciones por Gmail.

## Requisitos
- Credenciales configuradas para Gmail (cuenta con acceso SMTP/IMAP).
- Acceso a n8n con permisos para activar workflows y configurar nodos de error.

## Instrucciones de configuración
1. **Configurar credenciales de Gmail**
   - En n8n, dentro de _Credenciales_, añade y configura tu cuenta Gmail con permisos SMTP.
2. **Activar el nodo `ErrorTrigger`**
   - Este nodo se encargará de iniciar el workflow al detectar errores.
3. **Verificar configuraciones del nodo Gmail**
   - Asegúrate de que el usuario y destinatarios estén correctamente definidos para el envío de alertas.

## Detalles de funcionamiento
- El nodo `ErrorTrigger` captura errores generados en flujos específicos.
- Al activarse, el workflow procesa la información del error y utiliza el nodo `Gmail` para enviar una notificación automática.
- El workflow consta de 3 nodos que gestionan la captura, procesamiento y notificación del error.

## Ejemplos de uso
- Notificación inmediata ante fallos en agentes automatizados para abogados.
- Alerta por correo cuando un servicio relacionado falla o encuentra excepciones.
```
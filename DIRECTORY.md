# Datos para el directorio de Anthropic

Paquete preparado para presentación. Su presencia en GitHub no implica aprobación
ni publicación en el directorio de Anthropic.

## Plugin bundle

- Nombre: Identik.
- Repositorio: https://github.com/Identik-me/identik-claude-plugin
- Ruta del plugin: raíz; dejar vacía.
- Rama: `main`. Versión actual: `1.0.1`.
- Categoría sugerida: productividad / gestión de documentos.
- Contacto: contacto@identik.me.
- Descripción: `.claude-plugin/plugin.json`.
- Documentación, soporte, privacidad, condiciones y logo: README.
- Ejemplos comprobables: sección Ejemplos del README.

La versión 1.0.1 elimina los cinco campos de listado que el portal señalaba como
desconocidos y el PNG que generaba la nota de archivo binario. Conserva los
enlaces y el logo SVG en el README; el manifiesto ya no declara un icono para la
ficha del directorio. El campo estándar `homepage` apunta a esa documentación.
La validación local estricta pasa sin advertencias; añade la nota informativa
`PRIVACY_URL_MISSING` porque obtiene la política de privacidad del README.
La confirmación del resultado del portal requiere revalidar el nuevo commit.

## MCP connector

- Nombre: Identik.
- URL: https://claude-connect.identik.me/mcp
- Autenticación: OAuth 2.0 con PKCE; descubrimiento automático.
- Una conexión admite Firma Digital, Firma Electrónica o ambas.
- La persona ingresa tokens dedicados de su equipo en el consentimiento de Identik,
  fuera del chat. No es un inicio de sesión con usuario y contraseña.
- Permisos disponibles: `documents:read`, `documents:write`, `notifications:send`.
- Once herramientas. La firma humana se completa en la plataforma.

Los revisores necesitan cuentas de demostración aisladas y tokens vigentes,
entregados sólo por el canal privado del portal. No usar cuentas de clientes ni
publicar credenciales en este repositorio. No declarar que no requiere cuenta:
el uso real requiere una cuenta y los permisos correspondientes de Identik.

## Tratamiento de datos

- Procesa datos personales: sí; los nombres y contactos de destinatarios y los
  parámetros/resultados necesarios para la operación autorizada.
- Conserva la conexión: tokens de equipo cifrados y permisos OAuth hasta 30 días;
  tokens de acceso de una hora. No guarda copias persistentes de PDFs o resultados.
- Servicios: plataformas Identik y Cloudflare para alojamiento y OAuth. Anthropic
  recibe la selección de resultados del MCP. El paquete no configura otros MCP,
  comandos de shell, hooks ni telemetría propia.
- No está dirigido a menores de 18 años.
- Política: https://claude-connect.identik.me/privacy
- Condiciones: https://claude-connect.identik.me/terms
- Soporte: https://claude-connect.identik.me/support

Revise las preguntas y declaraciones efectivas del portal antes de enviarlas.
No sustituya la política completa por estas notas.

## Envío

Abra https://claude.ai/directory/manage con una cuenta y plan habilitados, conecte
GitHub y presente tanto **MCP connector** como **Plugin bundle**. Ejecute Validate
sobre el commit final, revise el tratamiento de datos y complete los pasos de
revisión. La validación local no reemplaza los controles del portal.

Instrucciones oficiales: https://claude.com/docs/plugins/submit.

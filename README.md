# FM Barbería · Maqueta interactiva

Propuesta visual y funcional de un sistema con marca propia. Incluye sitio de reservas y panel de administración. No es el sitio oficial de FM Barbería.

## Ejecutar

No necesita instalación de dependencias ni compilación. Desde esta carpeta:

```sh
python -m http.server 8080
```

Abrir `http://localhost:8080`. Si usás Windows y el comando anterior no existe, probar `py -m http.server 8080`.

También podés usar Live Server de tu editor. Servir por HTTP permite que el almacenamiento local funcione de forma consistente.

## Recorridos

- `/`: propuesta de sitio público.
- `/#panel`: panel de gestión.
- Crear un turno con datos ficticios desde la página pública y comprobarlo en la agenda.
- Elegir profesional, fecha y horario; se comprueban superposiciones por profesional.
- Modificar la reserva o cambiar su estado a Cancelado para liberar la disponibilidad.
- Revisar clientes, exportación CSV, servicios, cobros ficticios, reportes y vistas previas de emails.
- Cambiar identidad y rubro en Marca y ajustes. Cambiar de rubro restaura los datos de muestra.

## Alcance real

Es una maqueta frontend con lógica en JavaScript y almacenamiento `localStorage`, bajo la clave `fm-demo-v2`. Cada navegador conserva sus propios datos. No hay sincronización entre dispositivos ni protección real del panel.

Emails, recordatorios y cobros son simulados. No contiene credenciales ni realiza reservas en AgendaPro. Para usar con un negocio real falta un backend con autenticación, permisos, base de datos compartida, validación de disponibilidad transaccional y cola de correo.

Los cuatro profesionales y el catálogo se basan en información pública. Los clientes, turnos y cobros son ficticios. El horario de 08:00 a 20:00, de lunes a sábado, es un supuesto de demostración. El servicio Color tiene diferencias entre la tarifa principal y la descripción de origen; la interfaz pide confirmación.

## Archivos

| Archivo | Contenido |
|---|---|
| `index.html` | Entrada de la aplicación |
| `app.js` | Datos de muestra, recorridos y lógica local |
| `style.css` | Diseño general y adaptación responsive |
| `fm.css` | Identidad visual de FM |
| `assets/` | Logo y foto pública del local |

Las fuentes tipográficas se solicitan a Google Fonts; hay fuentes de respaldo si no hay conexión.

## Subir a GitHub

Crear un repositorio y subir **el contenido de esta carpeta**, con `index.html` en la raíz. No requiere subir los Excel de prospectos, conversaciones, credenciales ni metadatos del servicio donde se publicó la demo anterior.

Si vas a publicarlo como sitio estático con GitHub Pages, la raíz ya está preparada con `.nojekyll`; elegí la rama y la carpeta raíz como origen donde esté disponible esa modalidad. El panel seguirá siendo una demostración accesible para quien pueda ver el sitio: publicar el frontend no crea autenticación ni un backend.

## Referencias de marca

Relevamiento del 19/10/2026:

- https://fmbarberia1.site.agendapro.com/ar
- https://www.instagram.com/barberiafm_/

El logo, la fotografía y el nombre identifican al negocio de referencia; no se otorga una licencia sobre esos recursos. Esta carpeta no incluye una licencia de redistribución de la marca. No hay relación oficial confirmada con FM Barbería.

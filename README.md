# Marina Alvear — Código completo

Sitio de demostración desarrollado para Ernesto Capuzzi.

## Abrir y ejecutar en tu computadora

1. Descomprimí el ZIP en una carpeta.
2. Abrí la carpeta `Marina_Alvear` en VS Code o en tu editor.
3. Instalá Node.js si todavía no lo tenés. El proyecto requiere Node.js 22.13 o superior.
4. Abrí la terminal del editor, ubicada dentro de esa carpeta, y ejecutá:

```powershell
node --version
npx pnpm@11.25.0 install --frozen-lockfile
npx pnpm@11.25.0 dev
```

Abrí la dirección que muestra la terminal. El puerto local predeterminado es 5173.
Mantené la terminal abierta mientras editás. El navegador actualiza los cambios automáticamente.
Para detenerlo, presioná Ctrl+C en la terminal.

No abras `page.tsx` haciendo doble clic: este proyecto necesita su servidor local.
La primera instalación requiere conexión a Internet. El mapa utiliza servicios externos.

## Dónde editar

| Archivo | Contenido |
| --- | --- |
| `app/page.tsx` | Portada y secciones de la página principal. |
| `app/globals.css` | Colores, tipografía, espaciado y diseño responsive. |
| `lib/studio.ts` | Nombre, zona, servicios, preguntas y configuración del mapa. |
| `app/especialidades/[slug]/page.tsx` | Diseño común de las cuatro páginas de especialidades. |
| `components/site-header.tsx` | Cabecera, navegación y menú móvil. |
| `components/inquiry.tsx` | Formulario, mensajes de error, copia y descarga del borrador. |
| `lib/consultation.ts` | Reglas de validación y preparación de la consulta. |
| `components/location-map.tsx` | Mapa de referencia de Recoleta. |
| `components/questions.tsx` | Preguntas desplegables. |
| `app/layout.tsx` | Pie de página, metadatos y estructura general. |
| `public/office.webp` | Imagen de la portada. |
| `public/favicon.svg` | Ícono del sitio. |

Para cambiar la imagen conservando el mismo nombre, reemplazá `public/office.webp`.
Si usás otro nombre o formato, actualizá la ruta del `<img>` en `app/page.tsx`.

## Tecnologías

TypeScript, React, Tailwind CSS, Leaflet y Vinext.
Vinext utiliza Vite y una estructura compatible con Next.js. El proyecto incluye
los archivos de configuración y los componentes de interfaz necesarios.

## Comprobar y compilar

```powershell
npx pnpm@11.25.0 exec tsc --noEmit
npx pnpm@11.25.0 build
```

## Estado de la demo

- La identidad, los textos y las condiciones de atención son provisionales.
- La imagen del estudio es ilustrativa.
- El mapa muestra el barrio de Recoleta, no un domicilio profesional confirmado.
- El formulario prepara un borrador. No envía, agenda ni guarda consultas.
- Cambiar `whatsapp` o `email` en los datos por sí solo no conecta el envío.
- Para el lanzamiento real falta verificar los datos y conectar los contactos.

## Tu copia local y la web publicada

Los cambios en este paquete son locales y no actualizan automáticamente el sitio publicado.
La configuración `.openai/hosting.json` identifica el proyecto original, pero no contiene
credenciales de acceso. Este ZIP no incluye historial Git, dependencias instaladas ni archivos
con secretos. No necesitás una cuenta de ChatGPT para revisar y editar el código localmente.

Conservá los archivos de licencia incluidos con los componentes y Leaflet.

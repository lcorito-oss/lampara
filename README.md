# 💡 Lámpara de neón

Una lámpara de escritorio interactiva hecha con HTML, CSS y JavaScript puro. Se enciende y se apaga jalando el hilo, y tanto la pantalla como la luz se pueden cambiar de color.

Inspirada en el diseño "Neon Lamp Login Form".

## Características

- **Hilo interactivo:** jálalo hacia abajo (mouse o dedo) o dale un clic para encender y apagar.
- **Colores de la lámpara:** cambia el color de la pantalla en cualquier momento.
- **Colores de la luz:** cambia el color del foco, el cono de luz y el resplandor del fondo. Solo está disponible con la lámpara encendida.
- **Accesible:** el hilo se puede usar con el teclado (`Tab` para enfocarlo, `Enter` o `Espacio` para accionarlo).
- **Adaptable:** se ve bien en computadora y en celular.
- **Sin dependencias:** un solo archivo, sin librerías ni imágenes externas.

## Cómo usarla

1. Descarga o clona el repositorio.
2. Abre `index.html` (o `lampara.html`) en tu navegador.

No necesita instalación ni servidor.

## Controles

| Acción | Resultado |
| --- | --- |
| Jalar el hilo o hacer clic en él | Enciende o apaga la lámpara |
| Fila **Lámpara** (panel superior derecho) | Cambia el color de la pantalla |
| Fila **Luz** (panel superior derecho) | Cambia el color de la luz (solo encendida) |
| `Enter` / `Espacio` sobre el hilo | Enciende o apaga con el teclado |

## Personalización

Los colores disponibles están al inicio del bloque `<script>`:

```js
const shades = ["#3b4252", "#7a3b3b", "#2f5d62", "#6b4f2a", "#d9d4c7"]; // pantalla
const lights = ["#ffd27a", "#ff5fa2", "#5ee7ff", "#7dff9b", "#b388ff"]; // luz
```

Agrega, quita o cambia valores hexadecimales y los puntos del panel se generan solos.

Los colores base de la interfaz (`--bg`, `--panel`, `--c`, `--shade`, etc.) son variables CSS definidas en `:root`.

## Publicar con GitHub Pages

1. Renombra el archivo a `index.html` si quieres que sea la página principal.
2. Ve a **Settings → Pages**.
3. Elige la rama `main` y la carpeta `/ (root)`.
4. Tu página quedará en `https://tu-usuario.github.io/tu-repo/`.

## Estructura

```
.
├── index.html   # la lámpara (HTML, CSS y JS en un solo archivo)
└── README.md
```

## Ideas para seguir

- Agregar el formulario de login que aparece al encender la lámpara.
- Efecto de sonido al jalar el hilo.
- Guardar el último color elegido.

## Licencia

Proyecto personal. Agrega aquí la licencia que prefieras (por ejemplo, MIT).

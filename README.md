# 💡 Lámpara interactiva con formulario de login

Una escena hecha con HTML, CSS y JavaScript puro: una lámpara de escritorio articulada que se enciende y se apaga jalando la cadena. Al encenderla, su haz de luz ilumina un formulario de inicio de sesión. Al apagarla, el formulario desaparece por completo, como si cayera la noche.

Inspirada en el diseño "Neon Lamp Login Form". La lámpara y la pelota son dibujos originales hechos en SVG.

## Características

- **Lámpara articulada:** brazos de barras paralelas, resorte, tornillos en las uniones, pantalla cónica con ranuras y base redonda.
- **Cadena interactiva:** se jala con el mouse o el dedo, o con un clic. También funciona con teclado (`Tab` para enfocarla, `Enter` o `Espacio` para accionarla).
- **Haz de luz realista:** rayos finos que se abren en abanico desde la boca de la pantalla, con neblina suave dentro del haz y un charco de luz en el piso.
- **Pelota de juguete:** está junto a la lámpara y proyecta su sombra en la dirección contraria a la luz. La sombra se intensifica al encender.
- **Rueda de color para la luz:** 24 tonos y 5 anillos, del color intenso al pastel, con centro blanco. Cambia el foco, los rayos, el charco del piso, el resplandor del fondo, las chispas y el acento del formulario.
- **Colores de la lámpara:** cinco tonos para la pantalla, los brazos y la base.
- **Panel que se esconde solo:** se muestra 4 segundos al abrir la página y al encender o apagar, y se desvanece. Reaparece al pasar el mouse o tocar la esquina superior izquierda.
- **Formulario de login:** pestañas Entrar y Registro, botón para ver la contraseña, "Recordarme", y botones de Google, GitHub y Apple. Está oculto con la lámpara apagada y aparece con un desvanecido suave al encenderla.
- **Chispas flotantes** que aparecen con la luz encendida.
- **Adaptable** a computadora y celular.
- **Sin dependencias:** un solo archivo, sin librerías ni imágenes externas.

## Cómo usarla

1. Descarga o clona el repositorio.
2. Abre `index.html` en tu navegador.

No necesita instalación ni servidor.

## Controles

| Acción | Resultado |
| --- | --- |
| Jalar la cadena o hacer clic en ella | Enciende o apaga la lámpara |
| `Enter` / `Espacio` sobre la cadena | Enciende o apaga con el teclado |
| Esquina superior izquierda (mouse encima o toque) | Muestra el panel de colores |
| Puntos de la fila **Lámpara** | Cambian el color de la lámpara |
| Rueda de la fila **Luz** (solo encendida) | Cambia el color de la luz |
| Pestañas **Entrar** / **Registro** | Cambian el modo del formulario |

En celular, el primer toque sobre el panel oculto solo lo muestra, sin cambiar ningún color.

## Personalización

Los colores de la lámpara están al inicio del bloque `<script>`:

```js
const shades = ["#ece9e2", "#f2b8c6", "#9fd3d6", "#f3d089", "#2a2e37"];
```

La rueda de la luz se genera con 24 tonos y estos niveles de luminosidad, del anillo exterior al interior:

```js
const Ls = [50, 60, 70, 80, 90];
```

El tiempo que tarda el panel en esconderse (4 segundos) está en las funciones `wheelShow` y `pointerleave`, como `4000`.

Los colores base de la interfaz (`--bg`, `--panel`, `--c`, `--shade`, etc.) son variables CSS definidas en `:root`.

## Publicar con GitHub Pages

1. Asegúrate de que el archivo se llame `index.html` y esté en la raíz del repositorio.
2. Ve a **Settings → Pages**.
3. En "Build and deployment", elige *Deploy from a branch*, la rama `main` y la carpeta `/ (root)`.
4. Tu página quedará en `https://tu-usuario.github.io/tu-repo/`.

Si no ves los cambios después de subir una versión nueva, espera a que la ejecución en **Actions** termine con palomita verde y abre la página en una ventana de incógnito, o agrega `?v=2` al final de la URL. GitHub Pages y el navegador guardan copias en caché.

## Estructura

```
.
├── index.html   # la escena completa (HTML, CSS y JS en un solo archivo)
└── README.md
```

## Notas

- El formulario es solo visual: al enviarlo muestra un mensaje de demostración. Para usarlo de verdad, conecta el evento `submit` a tu propio servidor.
- Los botones de Google, GitHub y Apple no tienen ninguna acción asociada.

## Ideas para seguir

- Efecto de sonido al jalar la cadena.
- Guardar el último color elegido.
- Conectar el formulario a un servicio de autenticación.

## Licencia

Proyecto personal.

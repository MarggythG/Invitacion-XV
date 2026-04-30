# 🎩 Invitación XV Años - Alicia en el País de las Maravillas

Invitación electrónica interactiva para XV años con temática de "Alicia en el País de las Maravillas". Incluye pantalla de introducción animada, sobre interactivo, carta con múltiples secciones navegables, efecto de escritura con pluma, simulación de fluidos WebGL y música de fondo.

## ✨ Características

### Pantalla de Introducción
- **Gato Sonriente animado** (`sonriente.gif`) con efecto de flotación
- Al tocar, se desvanece con **onda expansiva de fluido WebGL** en tonos morados
- Inicia la **música de fondo** automáticamente al interactuar

### Sobre y Carta
- **Sobre animado** (`sobreAlice.png`) con texto "Te invito a un mundo mágico"
- Al tocar el sobre, se abre con transición y revela la **carta** (`carta alice.jpg`)
- La carta tiene **5 secciones navegables** (toca para avanzar):
  1. **Invitación** — Texto de bienvenida + nombre + cuenta regresiva en tiempo real
  2. **Celebración** — Fecha, hora, lugar con enlace a Google Maps
  3. **Dress Code** — Instrucciones de vestimenta
  4. **Lluvia de Sobres** — Información sobre regalos
  5. **Confirmación** — Datos de contacto para RSVP

### Efecto de Escritura con Pluma 🪶
- Cada sección se **escribe letra por letra** simulando una pluma
- **Cursor de pluma animado** que sigue el texto mientras aparece
- **Salpicaduras de tinta** sutiles al inicio de cada párrafo
- Pausas naturales en puntos, comas y signos de exclamación
- Solo se ejecuta la **primera vez** que aparece cada sección

### Efectos Visuales
- **WebGL Fluid Splash** (`splashCursor.js`) — Efecto de fluido interactivo que responde al mouse y al toque
- **Video de fondo** (`background.mp4`) con overlay oscuro
- **Estrellas parpadeantes** en el fondo
- Transiciones suaves entre secciones (fadeInUp / fadeOutUp)

### Audio
- **Música de fondo** (`Fondo-Sonido.mp3`) en loop, se inicia al primer toque
- Volumen al 40% para no ser intrusivo

### Diseño Responsivo
- Optimizado para **dispositivos móviles** (< 480px)
- Padding adaptativo para que el texto no se superponga con los bordes decorativos de la carta
- Countdown horizontal en móvil
- Tamaños de fuente reducidos proporcionalmente
- Touch events optimizados con `{ passive: true }`

## 📁 Estructura del Proyecto

```
├── index.html           # Archivo principal (HTML + CSS + JS integrado)
├── splashCursor.js      # Motor WebGL de simulación de fluidos
├── sonriente.gif        # GIF del Gato de Cheshire (intro)
├── sobreAlice.png       # Imagen del sobre
├── carta alice.jpg      # Imagen de fondo de la carta (pergamino)
├── background.mp4       # Video de fondo
├── background.jpg       # Imagen de fondo alternativa
├── Fondo-Sonido.mp3     # Música de fondo
├── CAMBIOS_RAPIDOS.md   # Guía de cambios rápidos
├── PERSONALIZACION.md   # Guía de personalización
└── README.md            # Este archivo
```

## 🚀 Cómo Usar

1. Abre `index.html` en un navegador (o despliega en un servidor web)
2. Toca el gato sonriente para entrar
3. Toca el sobre para abrirlo
4. Toca la carta para navegar entre las 5 secciones

> **Nota:** Para que el audio y video funcionen correctamente, se recomienda servir desde un servidor HTTP (por ejemplo `npx serve` o Live Server de VS Code).

## 🎨 Personalización

### Datos del evento

En `index.html`, busca y modifica:

| Dato | Valor actual | Dónde buscarlo |
|------|-------------|----------------|
| Nombre | Sara Juliana Zarate Forero | Clase `.invite-name` |
| Fecha | Lunes, 13 de Junio de 2026 | Sección Celebración |
| Hora | 7:30 PM | Sección Celebración |
| Lugar | Castillo del monosorio | Sección Celebración |
| Mapa | Google Maps link | `href` en sección Lugar |
| Teléfono | +34 123 456 789 | Sección Confirmación |
| Fecha countdown | 2026-06-15T17:00:00 | Variable `targetDate` en JS |
| Dress code | Evita vestir de azul | Sección Dress Code |

### Tipografías

Se usan dos fuentes de Google Fonts:
- **Dancing Script** — Texto general cursivo
- **Great Vibes** — Títulos y nombre destacado

### Colores principales

| Elemento | Color | Código |
|----------|-------|--------|
| Texto principal | Marrón oscuro | `#3a1f00` |
| Nombre | Rojo oscuro | `#8b1a1a` |
| Títulos | Marrón cálido | `#4a2c0a` |
| Etiquetas | Dorado | `#8b6914` |
| Hints | Marrón claro | `#6b3a1f` |

### Imágenes

Reemplaza los archivos manteniendo el mismo nombre:
- `sonriente.gif` — GIF de la pantalla de intro
- `sobreAlice.png` — Imagen del sobre
- `carta alice.jpg` — Fondo de la carta (pergamino)
- `background.mp4` — Video de fondo
- `Fondo-Sonido.mp3` — Música de fondo

## 🛠 Tecnologías

- **HTML5** / **CSS3** / **JavaScript** vanilla (sin frameworks)
- **WebGL** para simulación de fluidos (splashCursor.js)
- **Google Fonts** (Dancing Script, Great Vibes)
- **CSS Animations** y **Keyframes**
- **MutationObserver** para detectar cambios de estado
- **Audio API** para música de fondo

## 📱 Compatibilidad

- Chrome / Edge / Safari / Firefox (versiones modernas)
- iOS Safari y Android Chrome
- Requiere soporte WebGL para el efecto de fluidos
- Audio requiere interacción del usuario (política de navegadores)

# Rueda Libre

Ecosistema web de **Rueda Libre**, alquiler de bicicletas en Medellín, creado por **Nodo Digital**:

- **Rueda Libre v2.0**: sitio informativo en Bootstrap 5.3.
- **Rueda Nocturna**: landing de campaña (rutas guiadas de jueves a sábado) en Tailwind CSS v4.

Ambos comparten paleta, tipografía y datos de contacto, y se enlazan entre sí.

## Enlaces

- Sitio principal: `https://TU-USUARIO.github.io/rueda-libre/`
- Landing: `https://TU-USUARIO.github.io/rueda-libre/nocturna/`

(Reemplaza `TU-USUARIO` y activa GitHub Pages en Settings > Pages > rama `main`.)

## Mapa de páginas

```
rueda-libre/
├── index.html                  Inicio (hero, carrusel, flota, rutas, beneficios, CTA)
├── paginas/
│   ├── tarifas.html            Tablas de tarifas + aside
│   └── reservas.html           Formulario validado + modal de políticas
├── pruebas/catalogo-bootstrap.html   Laboratorio solo con Bootstrap CDN
├── css/styles.css              Variables --bs-*, clases propias
├── nocturna/
│   ├── index.html              Landing completa (modo oscuro, planes, inscripción)
│   ├── prototipo.html          Hero con Tailwind Play CDN
│   ├── componentes.html        Kit de componentes v0.1
│   └── src/input.css · output.css
├── img/                        logo.svg y capturas/
├── bitacora.txt                Trazabilidad técnica
└── README.md
```

## Stack

HTML5 · CSS3 · Bootstrap 5.3 · Bootstrap Icons · Tailwind CSS v4 · Google Fonts (Montserrat 700, Open Sans 400/600)

## Identidad

| Color | Hex |
|---|---|
| Verde Ruta | `#1E7A4F` |
| Naranja Pedal | `#F39A2B` |
| Azul Noche | `#14213D` |
| Crema | `#FAF6EF` |
| Gris Asfalto | `#5B6470` |
| Amarillo Farol | `#FFD166` |

Contraste mínimo 4.5:1 en texto normal. Verde Ruta no se usa como texto sobre Azul Noche (3,01:1).

## Bootstrap vs Tailwind

| Criterio | Bootstrap 5.3 | Tailwind v4 |
|---|---|---|
| Velocidad de montaje | Alta, componentes listos | Media, se compone con utilidades |
| Peso CSS (min) | 232 KB (31 KB gzip) + 80 KB JS | 20 KB (4 KB gzip) |
| Control visual | Hay que sobrescribir estilos | Total |
| Interactividad | Carrusel, modal y menú incluidos | No incluye JS |

**Recomendación:** Bootstrap para sitios informativos con componentes interactivos; Tailwind para páginas de campaña con diseño propio y poco peso.

## Capturas

Guarda tus capturas en `img/capturas/` y enlázalas aquí:

- Escritorio: `img/capturas/escritorio.png`
- Móvil: `img/capturas/movil.png`
- Modo oscuro: `img/capturas/oscuro.png`

## Desarrollo local

```bash
# Abrir con Live Server (puerto 5500) y, para recompilar Tailwind:
cd nocturna
npm install tailwindcss @tailwindcss/cli
npx @tailwindcss/cli -i src/input.css -o src/output.css --minify
```

## Aprendizajes clave

- Una petición HTTP: `GET` -> `200` si existe, `404` si no.
- Etiquetas semánticas antes que `<div>`.
- Sin `!important` ni estilos en línea: la especificidad se resuelve con clases.
- Validación nativa del navegador más estilos de Bootstrap.
- Mobile-first y modo oscuro con `dark:` cuidando el contraste.

## Créditos

Diseño y desarrollo: **Nodo Digital** para Rueda Libre.

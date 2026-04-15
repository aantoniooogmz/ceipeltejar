# 🏫 CEIP El Tejar — Web del centro

Repositorio oficial de los archivos HTML de la web del **CEIP El Tejar** (Fuengirola, Málaga), alojados en **GitHub Pages** e integrados en el WordPress de Averroes mediante iframes.

---

## 🌐 URL pública

```
https://aantoniooogmz.github.io/ceipeltejar/
```

---

## 📁 Estructura del repositorio

```
ceipeltejar/
│
├── inicio.html             → Página de inicio (hero, noticias, enseñanzas, servicios)
├── novedades.html          → Listado de noticias con buscador y paginación
├── planes-y-proyectos.html → Planes, proyectos y documentos del centro (PDFs)
├── contacto.html           → Formulario de contacto, mapa e información
│
└── README.md               → Este archivo
```

---

## 🔗 Cómo están integrados en WordPress (Averroes)

Cada HTML se incrusta en su página de WordPress mediante un **iframe**. Averroes no permite `<style>` ni `<script>` en el editor, por eso toda la lógica y el diseño vive aquí en GitHub Pages.

El código que se pega en cada página de WordPress es:

```html
<iframe
  src="https://aantoniooogmz.github.io/ceipeltejar/NOMBRE-DEL-ARCHIVO.html"
  width="100%"
  height="800"
  frameborder="0"
  scrolling="no"
  style="width:100%; border:none; display:block;">
</iframe>

<script>
window.addEventListener('message', function(e) {
  if (e.data && e.data.iframeHeight) {
    document.querySelector('iframe').style.height = e.data.iframeHeight + 'px';
  }
});
</script>
```

> ⚠️ El script de abajo es el que hace que el iframe se ajuste automáticamente a la altura del contenido. Sin él, aparecerá un scroll interno o se cortará la página.

---

## 📄 Páginas y sus URLs

| Página | Archivo | URL GitHub Pages | URL WordPress |
|--------|---------|-----------------|---------------|
| Inicio | `inicio.html` | [Ver](https://aantoniooogmz.github.io/ceipeltejar/inicio.html) | [Ver](https://blogsaverroes.juntadeandalucia.es/ceipeltejar/) |
| Novedades | `novedades.html` | [Ver](https://aantoniooogmz.github.io/ceipeltejar/novedades.html) | [Ver](https://blogsaverroes.juntadeandalucia.es/ceipeltejar/novedades/) |
| Planes y Proyectos | `planes-y-proyectos.html` | [Ver](https://aantoniooogmz.github.io/ceipeltejar/planes-y-proyectos.html) | [Ver](https://blogsaverroes.juntadeandalucia.es/ceipeltejar/planes-y-proyectos/) |
| Contacto | `contacto.html` | [Ver](https://aantoniooogmz.github.io/ceipeltejar/contacto.html) | [Ver](https://blogsaverroes.juntadeandalucia.es/ceipeltejar/contactar-con-el-centro/) |

---

## 📦 PDFs del centro

Los documentos PDF están alojados en **Google Drive** (por límite de tamaño de GitHub) y enlazados desde `planes-y-proyectos.html`.

| Documento | Enlace |
|-----------|--------|
| Asambleas | [Abrir](https://drive.google.com/file/d/1dEJGJuAAFnNXbLUQE5qx6u1_NYmw-mv-/view) |
| Atención Educativa | [Abrir](https://drive.google.com/file/d/18SnmxXNqSVX_RIwdnxEyVCIc8ZMRBckK/view) |
| Itinerario Matemáticas | [Abrir](https://drive.google.com/file/d/1BspJCI1_arYlxn2w8doS3ceNsKMSUI--/view) |
| Patios Inclusivos | [Abrir](https://drive.google.com/file/d/1wIeB7G6VYSQezxGKNCtvZXtP_PHjhbkl/view) |
| PGC | [Abrir](https://drive.google.com/file/d/1qHcHiQgVa5Z8b6fLhcVYw3mXGpp0HfBt/view) |
| Plan de Centro 25/26 | [Abrir](https://drive.google.com/file/d/1LeXhIt4TarD8A-67XGyk4gx9ZUTxO9OP/view) |
| Programa Acogida y Tránsito 25/26 | [Abrir](https://drive.google.com/file/d/1Widf3aOUBFF3gaWE8k4al0YrbjgCVldv/view) |
| ROF | [Abrir](https://drive.google.com/file/d/1y2uiE3rllb4y6KxFuZv2l0WxLnbj6MV0/view) |

> Para añadir un nuevo PDF: súbelo a Google Drive, ponlo en modo "Cualquier persona con el enlace puede ver" y añade el enlace en `planes-y-proyectos.html`.

---

## ✏️ Cómo editar una página

1. Abre el archivo `.html` correspondiente
2. Haz los cambios directamente en el código
3. En GitHub: ve al archivo → icono del lápiz ✏️ → edita → **Commit changes**
4. Los cambios se publican automáticamente en 1-2 minutos

> Si el archivo es grande (más de 25 MB), clona el repositorio en local y haz push.

---

## 🎨 Sistema de diseño

Todas las páginas comparten el mismo sistema visual:

| Elemento | Valor |
|----------|-------|
| Fuente títulos | `Fraunces` (Google Fonts) |
| Fuente texto | `Nunito` (Google Fonts) |
| Verde principal | `#3a9e4f` |
| Azul | `#3b82c4` |
| Naranja | `#e8831a` |
| Amarillo | `#f5c842` |
| Franja top | Degradado animado con los 4 colores |

---

## ⚙️ Cómo funciona el autoajuste de altura del iframe

Cada HTML incluye este script al final:

```javascript
function sendHeight() {
  window.parent.postMessage({ iframeHeight: document.body.scrollHeight }, '*');
}
window.addEventListener('load', sendHeight);
window.addEventListener('resize', sendHeight);
```

Y en la página de WordPress debe estar el script receptor (ver sección de integración arriba). Esto evita que aparezca scroll dentro del iframe y hace la página responsive.

---

## 🔄 Cómo añadir una página nueva

1. Crea un nuevo archivo `.html` basándote en cualquiera de los existentes
2. Mantén el mismo sistema de colores y fuentes
3. Añade al final el script de autoajuste de altura
4. Súbelo al repositorio
5. En WordPress, crea una página nueva y pega el iframe apuntando a la nueva URL

---

## 👤 Mantenimiento

Este repositorio fue creado y configurado durante el curso **2025/26** como parte del proyecto de prácticas de **Sistemas Microinformáticos y Redes (SMR)** en el CEIP El Tejar.

Para cualquier duda técnica sobre la estructura del repositorio o la integración con WordPress, contactar con el equipo TIC del centro.

---

*CEIP El Tejar · Fuengirola, Málaga · Junta de Andalucía*

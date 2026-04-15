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
├── index.html                  → Redirección automática a inicio.html
├── inicio.html                 → Página de inicio (hero, noticias, enseñanzas, servicios)
├── novedades.html              → Listado de noticias con buscador y paginación
├── contacto.html               → Formulario de contacto, mapa e información
│
├── asi-somos.html              → Historia e información general del centro
├── claustro.html               → Directorio del claustro de profesores
├── planes-y-proyectos.html     → Planes, proyectos y documentos del centro (PDFs)
│
├── infantil.html               → 2º Ciclo de Educación Infantil (3–6 años)
├── primaria1.html              → 1º Ciclo de Educación Primaria (6–8 años)
├── primaria2.html              → 2º Ciclo de Educación Primaria (8–10 años)
├── primaria3.html              → 3º Ciclo de Educación Primaria (10–12 años)
│
├── aula-matinal.html           → Información sobre el aula matinal
├── comedor.html                → Información sobre el comedor escolar
├── extraescolares.html         → Actividades extraescolares
│
├── biblioteca.html             → Biblioteca escolar
├── ampa.html                   → AMPA del centro
├── idiomas.html                → Programa de idiomas
│
└── README.md                   → Este archivo
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

> ⚠️ El script es el que hace que el iframe se ajuste automáticamente a la altura del contenido. Sin él, aparecerá scroll interno o se cortará la página.

---

## 📄 Páginas y sus URLs

| Página | Archivo | URL GitHub Pages | URL WordPress |
|--------|---------|-----------------|---------------|
| Inicio | `inicio.html` | [Ver](https://aantoniooogmz.github.io/ceipeltejar/inicio.html) | [Ver](https://blogsaverroes.juntadeandalucia.es/ceipeltejar/) |
| Novedades | `novedades.html` | [Ver](https://aantoniooogmz.github.io/ceipeltejar/novedades.html) | [Ver](https://blogsaverroes.juntadeandalucia.es/ceipeltejar/novedades/) |
| Contacto | `contacto.html` | [Ver](https://aantoniooogmz.github.io/ceipeltejar/contacto.html) | [Ver](https://blogsaverroes.juntadeandalucia.es/ceipeltejar/contactar-con-el-centro/) |
| Así somos | `asi-somos.html` | [Ver](https://aantoniooogmz.github.io/ceipeltejar/asi-somos.html) | [Ver](https://blogsaverroes.juntadeandalucia.es/ceipeltejar/asi-somos/) |
| Claustro | `claustro.html` | [Ver](https://aantoniooogmz.github.io/ceipeltejar/claustro.html) | [Ver](https://blogsaverroes.juntadeandalucia.es/ceipeltejar/claustro-escolar/) |
| Planes y Proyectos | `planes-y-proyectos.html` | [Ver](https://aantoniooogmz.github.io/ceipeltejar/planes-y-proyectos.html) | [Ver](https://blogsaverroes.juntadeandalucia.es/ceipeltejar/planes-y-proyectos/) |
| Ed. Infantil | `infantil.html` | [Ver](https://aantoniooogmz.github.io/ceipeltejar/infantil.html) | [Ver](https://blogsaverroes.juntadeandalucia.es/ceipeltejar/2o-ciclo-de-educacion-infantil/) |
| 1º Ciclo Primaria | `primaria1.html` | [Ver](https://aantoniooogmz.github.io/ceipeltejar/primaria1.html) | [Ver](https://blogsaverroes.juntadeandalucia.es/ceipeltejar/1o-ciclo-de-educacion-primaria/) |
| 2º Ciclo Primaria | `primaria2.html` | [Ver](https://aantoniooogmz.github.io/ceipeltejar/primaria2.html) | [Ver](https://blogsaverroes.juntadeandalucia.es/ceipeltejar/2o-ciclo-de-educacion-primaria/) |
| 3º Ciclo Primaria | `primaria3.html` | [Ver](https://aantoniooogmz.github.io/ceipeltejar/primaria3.html) | [Ver](https://blogsaverroes.juntadeandalucia.es/ceipeltejar/3o-ciclo-de-educacion-primaria/) |
| Aula Matinal | `aula-matinal.html` | [Ver](https://aantoniooogmz.github.io/ceipeltejar/aula-matinal.html) | [Ver](https://blogsaverroes.juntadeandalucia.es/ceipeltejar/aula-matinal/) |
| Comedor | `comedor.html` | [Ver](https://aantoniooogmz.github.io/ceipeltejar/comedor.html) | [Ver](https://blogsaverroes.juntadeandalucia.es/ceipeltejar/comedor-escolar/) |
| Extraescolares | `extraescolares.html` | [Ver](https://aantoniooogmz.github.io/ceipeltejar/extraescolares.html) | [Ver](https://blogsaverroes.juntadeandalucia.es/ceipeltejar/actividades-extraescolares/) |
| Biblioteca | `biblioteca.html` | [Ver](https://aantoniooogmz.github.io/ceipeltejar/biblioteca.html) | [Ver](https://blogsaverroes.juntadeandalucia.es/ceipeltejar/biblioteca/) |
| AMPA | `ampa.html` | [Ver](https://aantoniooogmz.github.io/ceipeltejar/ampa.html) | [Ver](https://blogsaverroes.juntadeandalucia.es/ceipeltejar/ampa/) |
| Idiomas | `idiomas.html` | [Ver](https://aantoniooogmz.github.io/ceipeltejar/idiomas.html) | [Ver](https://blogsaverroes.juntadeandalucia.es/ceipeltejar/idiomas/) |

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

> Para añadir un nuevo PDF: súbelo a Google Drive → click derecho → Compartir → "Cualquier persona con el enlace" → copia el enlace y añádelo en `planes-y-proyectos.html`.

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
| Border radius tarjetas | `14px` |
| Border radius sección | `20px` |

---

## ✏️ Cómo editar una página existente

1. Entra al repositorio en [github.com/aantoniooogmz/ceipeltejar](https://github.com/aantoniooogmz/ceipeltejar)
2. Haz click en el archivo `.html` que quieres editar
3. Pulsa el icono del lápiz ✏️ (arriba a la derecha)
4. Haz los cambios en el código
5. Pulsa **Commit changes** → confirma
6. En 1–2 minutos los cambios están publicados en GitHub Pages

---

## ➕ Cómo añadir una página nueva

1. Copia el contenido de una página existente como base
2. Cambia el contenido manteniendo el mismo sistema de colores y fuentes
3. Asegúrate de que al final del HTML está el script de autoajuste:

```javascript
function sendHeight() {
  window.parent.postMessage({ iframeHeight: document.body.scrollHeight }, '*');
}
window.addEventListener('load', sendHeight);
window.addEventListener('resize', sendHeight);
const mo = new MutationObserver(sendHeight);
mo.observe(document.body, { childList: true, subtree: true, attributes: true });
```

4. Sube el archivo al repositorio
5. En WordPress, crea la página y pega el iframe con la nueva URL
6. Añade la página a la tabla de este README

---

## ⚠️ Cosas importantes a tener en cuenta

- **Todos los enlaces** dentro de los HTML deben llevar `target="_top"` para que al hacer click se abra la página en la ventana principal y no dentro del iframe
- **Los PDFs grandes** no se pueden subir a GitHub (límite 25 MB) → usar siempre Google Drive
- **Las noticias** de `novedades.html` e `inicio.html` se cargan automáticamente desde la API de WordPress del colegio, no hay que tocarlas manualmente
- **Averroes** no permite `<style>` ni `<script>` en el editor de páginas → todo el código va en los HTML de GitHub Pages

---

## 👤 Mantenimiento

Este repositorio fue creado y configurado durante el curso **2025/26** como parte del proyecto de prácticas de **Sistemas Microinformáticos y Redes (2º SMR)** en el CEIP El Tejar.

Para cualquier duda técnica sobre la estructura del repositorio o la integración con WordPress, contactar con el equipo TIC del centro a través de [29009651.edu@juntadeandalucia.es](mailto:29009651.edu@juntadeandalucia.es).

---

*CEIP El Tejar · Fuengirola, Málaga · Junta de Andalucía · Curso 2025/26*

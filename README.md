# 📻 EchoBarrio — Banco de Sonidos Comunitario & Muestra en Vivo

**EchoBarrio** es una plataforma web interactiva de memoria sonora abierta diseñada para capturar, archivar, descargar y remezclar en vivo los paisajes sonoros de la comunidad (pregones, voces, coros y sonidos ambientales del río, el puerto y la plaza).

Desarrollado para la muestra del **27 al 29 de noviembre** en Puerto Boyacá, Boyacá.

---

## 🎯 Características Principales

1. **Archivo / Banco de Samples Abierto:**
   - Reproductor rápido con visualización de onda.
   - Búsqueda en tiempo real y filtrado por categorías (*Ambiente / Río*, *Pregones / Puerto*, *Voces & Historia*, *Coros & Ritmo*).
   - Descarga directa de muestras bajo licencia abierta **Creative Commons (CC BY 4.0)**.
2. **Aporte Ciudadano desde el Celular:**
   - Grabación directa con micrófono desde el navegador (límite de 15 segundos) o subida de archivos de audio (máx. 5 MB).
   - Etiquetado de título, categoría, lugar/barrio y autoría.
   - Flujo de **autorización legal obligatoria** (licencia CC BY 4.0, consentimiento expreso de voces y acudientes de menores, declaración de ausencia de música protegida y tratamiento de datos).
3. **Muestra en Vivo (Modo Proyección):**
   - Generación automática de **Código QR** apuntando a la URL activa para participación inmediata del público sin instalar aplicaciones.
   - **Grid de 12 Sampler Pads** táctiles para disparo de muestras en tiempo real junto al productor local.
   - Reproductor integrado para piezas musicales y *beats* producidos con el banco comunitario.
4. **Panel de Moderación y Administración:**
   - Filtro previo de aprobación para evitar contenido irrespetuoso o con derechos de autor.
   - Gestión y eliminación de audios publicados en el banco abierto.

---

## 🛠️ Arquitectura y Tecnologías

El proyecto está construido como una **Single Page Application (SPA) estática**, sin dependencias de compilación ni servidores complejos, facilitando su preservación y transferencia institucional:

* **Frontend:** HTML5, Tailwind CSS (vía CDN), JavaScript Vanilla (ES6+).
* **Audio:** Web Audio API & HTML5 MediaRecorder API.
* **Iconografía y QR:** Lucide Icons & QRCode.js.
* **Persistencia:** 
  * *Modo Demo Local:* `localStorage` del navegador (funciona sin conexión a internet como respaldo en vivo).
  * *Modo Nube:* Integración lista para **Supabase** (PostgreSQL + Storage).

---

## 🚀 Instalación y Despliegue (GitHub Pages)

1. Clona o descarga este repositorio.
2. Asegúrate de mantener el archivo principal `index.html` en la raíz del proyecto.
3. En GitHub, ve a **Settings > Pages**, selecciona la rama `main` y carpeta `/ (root)` y guarda los cambios.
4. Tu instancia quedará publicada con certificado **HTTPS** (requerido por los navegadores móviles para habilitar el acceso al micrófono).

### Conexión a Base de Datos en la Nube (Supabase)
1. Crea un proyecto gratuito en [Supabase](https://supabase.com).
2. Crea un bucket público en **Storage** llamado `audios` con políticas de lectura e inserción públicas.
3. Crea la tabla `sonidos` en el **SQL Editor** con los campos: `id`, `created_at`, `titulo`, `tipo`, `lugar`, `autor`, `audio_url`, `aprobado`.
4. Abre la web publicada, haz clic en el botón de **Configuración (⚙️)** en la barra superior e ingresa tu `Supabase URL` y `Anon Key`.

---

## 🤖 Declaración sobre el Uso de Inteligencia Artificial

En cumplimiento con los lineamientos de transparencia de la convocatoria:
* **Programación:** Se utilizaron herramientas de Inteligencia Artificial generativa exclusivamente como asistente de desarrollo para estructurar la interfaz HTML/CSS y depurar la lógica de captura de audio en JavaScript.
* **Contenido Sonoro:** **El 100% de los sonidos, voces, pregones y paisajes sonoros archivados en esta plataforma son grabaciones reales realizadas por personas de la comunidad.** Ningún audio fue generado sintéticamente mediante IA.

---

## 🔄 Guía de Transferencia del Proyecto

Para ceder la titularidad técnica completa de la plataforma a la entidad organizadora:
1. **Repositorio de Código:** En GitHub, ir a `Settings > General > Danger Zone > Transfer ownership` e ingresar el usuario/organización oficial de la entidad.
2. **Base de Datos y Archivos:** En Supabase, ir a `Project Settings > General > Transfer project` para transferir el almacenamiento de audios y registros.

---

## 📄 Licencias

* **Código Fuente:** Distribuido bajo la **Licencia MIT** (permite uso, copia, modificación y distribución libre por parte de la entidad y la comunidad).
* **Banco de Sonidos (Aportes Comunitarios):** Publicados bajo **Creative Commons Atribución 4.0 Internacional (CC BY 4.0)**.

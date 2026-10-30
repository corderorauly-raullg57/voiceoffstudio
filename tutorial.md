# VoiceOFF Studio — Tutorial

**VoiceOFF Studio** convierte tus textos en locuciones profesionales en español, con emociones, música de fondo y exportación a WAV o MP3.
Funciona **dentro del navegador** (Chrome o Edge) y, una vez instaladas las voces, **sin internet**.

---

## Índice

1. [Requisitos](#1-requisitos)
2. [Primera vez: instalar el motor y las voces](#2-primera-vez-instalar-el-motor-y-las-voces)
3. [La pantalla, parte por parte](#3-la-pantalla-parte-por-parte)
4. [Tu primera locución en 1 minuto](#4-tu-primera-locución-en-1-minuto)
5. [Pestaña Voz](#5-pestaña-voz)
6. [Pestaña Biblioteca](#6-pestaña-biblioteca)
7. [Pestaña Sonido](#7-pestaña-sonido)
8. [Pestaña Música](#8-pestaña-música)
9. [Pestaña Exportar](#9-pestaña-exportar)
10. [Pestaña Proyecto](#10-pestaña-proyecto)
11. [Secciones: varias voces en un mismo audio](#11-secciones-varias-voces-en-un-mismo-audio)
12. [Copia de seguridad y uso en otra PC](#12-copia-de-seguridad-y-uso-en-otra-pc)
13. [Atajos de teclado](#13-atajos-de-teclado)
14. [Consejos para que suene mejor](#14-consejos-para-que-suene-mejor)
15. [Problemas frecuentes](#15-problemas-frecuentes)

---

## 1. Requisitos

| | |
|---|---|
| **Navegador** | Google Chrome o Microsoft Edge (recomendados). Firefox funciona, pero no permite elegir carpetas. |
| **Equipo** | Cualquier PC con Windows, Linux o Mac. Con 4 GB de RAM es suficiente. |
| **Internet** | Solo para descargar el motor y las voces la primera vez. Después no hace falta. |
| **Espacio** | Unos 12 MB para el motor y entre 27 y 110 MB por cada voz. |

> Abre siempre el archivo **`VoiceOFF.html`** desde la misma carpeta y con el mismo navegador. Las voces instaladas quedan guardadas en ese navegador.

---

## 2. Primera vez: instalar el motor y las voces

Para hablar, la app necesita dos cosas:

- **El motor de voz** (unos 12 MB, se instala una sola vez).
- **Al menos una voz española**.

Hay dos formas de instalarlas.

### Opción A — Con internet, desde la app

1. Abre `VoiceOFF.html` con Chrome.
2. Ve a la pestaña **Biblioteca**.
3. En **«Motor de voz español»**, pulsa **Descargar**.
4. En **«Voces en español»**, pulsa **Descargar** en la voz que quieras.
5. Cuando veas **«✅ Listo para trabajar sin internet»**, ya puedes usarla.

> **Si se corta internet o se va la corriente**, no pasa nada: vuelve a pulsar el botón (dirá **Continuar**) y la descarga sigue donde quedó.
>
> **En Cuba y otros países con bloqueo**, conecta la VPN antes de descargar las voces. Si Hugging Face no abre, cambia la fuente a **«Espejo (hf-mirror)»** en el selector de arriba a la derecha de la Biblioteca.

### Opción B — Sin internet, desde archivos

Sirve si ya tienes los archivos en una carpeta, una memoria USB o porque los bajaste con un gestor de descargas.

1. Ve a **Biblioteca**.
2. Pulsa **Importar carpeta…** y elige la carpeta donde están los archivos.
   También puedes usar **Importar archivos…** y seleccionarlos a mano.
3. En unos segundos aparece **«✅ Listo para trabajar sin internet»**.

**Archivos que reconoce la app:**

| Tipo | Archivos |
|---|---|
| Motor (obligatorio) | `ort.wasm.min.mjs`, `ort-wasm-simd-threaded.mjs`, `ort-wasm-simd-threaded.wasm`, `piper_phonemize.js`, `piper_phonemize.wasm`, `piper_phonemize.data` |
| Codificador MP3 | `lame.min.js` |
| Cada voz (2 archivos) | `nombre-de-la-voz.onnx` y `nombre-de-la-voz.onnx.json` |

> **¿Quieres bajarlos con un gestor de descargas?** En **Biblioteca → «Ver enlaces para gestor de descargas»** tienes todos los enlaces directos. Puedes copiarlos o guardarlos en un `.txt`. Free Download Manager o IDM reanudan las descargas si se cortan.

### Voces disponibles

| Voz | Acento | Calidad | Tamaño |
|---|---|---|---|
| **Dave** | España | Media | ≈ 60 MB |
| **Sharvard** | España | Media · 2 locutores (hombre y mujer) | ≈ 73 MB |
| **Claude** | México | Alta | ≈ 60 MB |
| **Ald** | México | Media | ≈ 60 MB |
| **Daniela** | Argentina | Alta | ≈ 109 MB |
| **Carl** | España | Ligera y rápida | ≈ 27 MB |

---

## 3. La pantalla, parte por parte

```
┌──────────────────────────────────────────────────────────────────┐
│  VoiceOFF Studio        Motor · Voces del sistema · En línea      │  ← barra superior
├──────────────────────────────────────┬───────────────────────────┤
│  GUION                               │  Voz · Biblioteca · Sonido │
│  (aquí escribes tu texto)            │  Música · Exportar ·       │  ← panel de ajustes
│                                      │  Proyecto                  │
│  caracteres · palabras · duración    │                            │
├──────────────────────────────────────┤                            │
│  SECCIONES (opcional)                │                            │
└──────────────────────────────────────┴───────────────────────────┘
│ ▶  ■   00:12 / 00:23   ▁▃▅▇▅▃▁ onda ▁▃▅   ▮▮▮▮ nivel   ↻ Generar │  ← reproductor
└──────────────────────────────────────────────────────────────────┘
```

- **Barra superior:** muestra la voz activa, cuántas voces tiene tu sistema y si hay conexión.
- **Guion:** el texto que se va a locutar. Debajo verás los caracteres, las palabras y la duración aproximada.
- **Secciones:** sirven para dividir el guion y ponerle una voz distinta a cada parte.
- **Panel de ajustes:** las 6 pestañas con todas las opciones.
- **Reproductor (abajo):**
  - **▶ / ⏸** reproduce o pausa.
  - **■** detiene.
  - **La onda** muestra el audio. Haz clic en cualquier punto para saltar ahí.
  - **El medidor** muestra el nivel de volumen: verde está bien, amarillo es alto y rojo está al límite.
  - **↻ Generar** vuelve a crear el audio con los ajustes actuales.

---

## 4. Tu primera locución en 1 minuto

1. Escribe o pega tu texto en **Guion**. También puedes elegir uno de **«Cargar ejemplo…»**.
2. En la pestaña **Voz**, elige **Español offline** y la voz que prefieras.
3. Elige una **emoción**, por ejemplo **Noticia** o **Cálido**.
4. Pulsa **▶** o **↻ Generar** y escucha.
5. Ve a **Exportar**, elige **MP3** o **WAV** y pulsa **Exportar audio**.
6. Pulsa **Descargar**. Listo.

---

## 5. Pestaña Voz

### Motor de voz

| Motor | Para qué sirve |
|---|---|
| **Español offline** | Las voces neuronales instaladas en la Biblioteca. Suenan naturales y **se pueden exportar**. Es el que usarás para trabajar. |
| **Sistema** | Las voces que trae tu Windows. Suenan al instante, pero **el navegador no deja grabarlas**: sirven solo para escuchar un borrador rápido. Al exportar, la app usa automáticamente la voz offline. |

### Voz y locutor

- **Voz:** elige entre las voces que tienes instaladas.
- **Locutor:** solo aparece en las voces que traen varios, como **Sharvard** (M = hombre, F = mujer).
- **▶ Probar voz:** dice una frase corta para que escuches cómo suena.

### Emociones

Cada emoción ajusta de una vez la velocidad, el tono, las pausas, la ecualización, la sala y la expresividad:

| Emoción | Ideal para |
|---|---|
| 🙂 **Neutral** | Uso general, tutoriales |
| 😄 **Alegre** | Publicidad, redes sociales |
| 😔 **Triste** | Relatos, momentos emotivos |
| 😠 **Enojado** | Personajes, dramatizaciones |
| 🤫 **Susurro** | Misterio, ASMR, intimidad |
| 🏔️ **Épico** | Tráileres, presentaciones grandes |
| 📻 **Noticia** | Noticieros, anuncios formales |
| 🤗 **Cálido** | Meditación, cuentos, atención al cliente |

Después de elegir una emoción puedes retocar cualquier control a mano.

### Velocidad y tono

- **Velocidad:** de 0,5× (muy lento) a 1,6× (rápido). Cambiar la velocidad **no** altera el tono de la voz.
- **Tono:** más grave (−) o más agudo (+), en semitonos.

> **Truco:** haz **doble clic sobre el número** de cualquier control para devolverlo a su valor original.

---

## 6. Pestaña Biblioteca

Es el **gestor de voces**. Desde aquí:

- Ves el estado: **«Listo para trabajar sin internet»** o qué falta por instalar.
- Ves cuánto espacio ocupa la app.
- **① Descargar con internet:** instalar el motor y las voces. Las descargas se reanudan si se cortan.
- **② Sin internet:** importar archivos o carpetas, o ver los enlaces directos para tu gestor de descargas.
- **▶** junto a una voz instalada: escucharla.
- **✕** junto a una voz instalada: eliminarla para liberar espacio.
- **Guardar copia de todo en una carpeta…:** saca todos los archivos instalados a una carpeta (ver el [punto 12](#12-copia-de-seguridad-y-uso-en-otra-pc)).

---

## 7. Pestaña Sonido

| Control | Qué hace |
|---|---|
| **Pausa entre frases** | Silencio real entre frase y frase. Más pausa suena más pausado y solemne. |
| **Expresividad** | Varía un poco la entonación en cada frase para que no suene plano ni robótico. |
| **Volumen de voz** | Volumen de la voz respecto a la música. |
| **Graves** | Da cuerpo a la voz y la hace más «de radio». |
| **Agudos** | Da claridad y presencia. |
| **Reverberación** | Simula una sala. Poca suena a estudio; mucha, a iglesia o salón grande. |
| **Eco** | Repetición de la voz, para efectos especiales. |

**Restablecer según emoción** devuelve todos estos controles a los valores de la emoción elegida.

> La app aplica automáticamente un **compresor** y un **limitador** profesionales para que la voz suene pareja y nunca se sature.

---

## 8. Pestaña Música

### Estilos incluidos

La música **se genera en el momento** y es **libre de derechos**: puedes usarla en trabajos para clientes.

| Estilo | Carácter |
|---|---|
| **Sin música** | Solo voz |
| **Relax** | Pad cálido y tranquilo |
| **Épica** | Cinematográfica, con percusión |
| **Lo-Fi** | Nocturna, con textura de vinilo |
| **Corporativa** | Optimista, para empresas |
| **Tensión** | Dron oscuro, suspenso |
| **Alegre** | Luminosa y rítmica |
| **Mi archivo** | Tu propio MP3 o WAV |

- **▶ Escuchar música:** la oyes sola. Pulsa **■** para parar.
- **Subir MP3/WAV…:** usa una canción tuya. Asegúrate de tener derechos para usarla.

### Controles

| Control | Qué hace |
|---|---|
| **Volumen de la música** | Nivel general de la música. Entre 15 % y 25 % suele ir bien. |
| **Ducking** | La música **baja sola cuando se habla** y sube en los silencios, como en la radio. |
| **Fundido de entrada** | Segundos que tarda la música en aparecer al inicio. |
| **Fundido de salida** | Segundos que tarda en desaparecer al final. |

---

## 9. Pestaña Exportar

1. **Formato:**
   - **WAV:** sin pérdida, máxima calidad. Ideal para edición de vídeo.
   - **MP3:** 128 kbps, ocupa poco. Ideal para WhatsApp, redes y web.
2. **Frecuencia de muestreo:**
   - **44,1 kHz:** estándar de audio.
   - **48 kHz:** estándar de vídeo.
   - **22 kHz:** archivo más ligero.
3. **Normalizar volumen a −1 dB:** déjalo marcado para que el audio suene fuerte y sin distorsión.
4. Pon el **nombre del archivo** en la casilla **Archivo** (debajo del guion).
5. Pulsa **Exportar audio** y después **Descargar**.

### Historial

Los **últimos 12 audios** que exportes quedan guardados en la app. Desde el historial puedes:

- **⬇** descargarlo de nuevo.
- **📁** guardarlo en la carpeta de trabajo.
- **✕** quitarlo del historial.

---

## 10. Pestaña Proyecto

### Guardar y abrir proyectos

- **Guardar proyecto:** crea un archivo `.voiceoff.json` con el guion, las secciones y **todos** los ajustes.
- **Abrir proyecto…:** lo recupera tal cual para seguir trabajando otro día o en otra PC.

> Además, la app **guarda sola** tu guion y tus ajustes mientras trabajas. Si se va la corriente, al volver a abrirla todo sigue ahí.

### Carpeta de trabajo (Chrome / Edge)

- **Conectar carpeta…:** elige una carpeta, por ejemplo `Documentos\Locuciones`.
  A partir de ahí, cada audio exportado y cada proyecto se guarda **directamente** en esa carpeta.
- **Historial → carpeta:** copia todo el historial a la carpeta de una vez.

---

## 11. Secciones: varias voces en un mismo audio

Útil para **diálogos**, **cuñas con dos locutores** o **podcasts**.

1. Escribe el guion separando las partes con **una línea en blanco** o con `===`.
2. Pulsa **Dividir guion en secciones**.
3. En cada sección:
   - Cambia el **título** (por ejemplo «Presentador» o «Cliente»).
   - Elige su **voz** en el desplegable.
   - **▶ Escuchar:** oye solo esa sección.
   - **↻ Regenerar:** vuelve a sintetizar solo esa parte.
   - **↑ ↓:** cambia el orden.
   - **✕:** elimina la sección.
4. Deja marcado **«Usar secciones»** y pulsa **↻ Generar** o **Exportar audio**.

La etiqueta **✓ sintetizada** indica que esa sección ya está lista, así que no se vuelve a calcular. Si cambias el texto de una sola sección, solo se rehace esa.

**Ejemplo de diálogo:**

```
¡Hola! ¿Ya conoces la nueva panadería del barrio?

===

Claro que sí. Su pan de leche es el mejor de la ciudad.

===

Panadería La Espiga. Abierta todos los días desde las siete de la mañana.
```

Con **Sharvard** puedes poner el locutor **F** en la primera sección y el **M** en la segunda.

---

## 12. Copia de seguridad y uso en otra PC

Las voces que descargas desde la app quedan **dentro del navegador**, no como archivos sueltos. Para no tener que descargarlas nunca más:

### Sacar la copia

1. **Biblioteca → «Guardar copia de todo en una carpeta…»**
2. Elige una carpeta, por ejemplo `VoiceOFF-archivos` o una memoria USB.
3. Acepta el permiso de Chrome.

La app guarda ahí el motor y todas las voces como archivos normales.

### Instalar en otra PC sin internet

1. Copia la carpeta completa, con `VoiceOFF.html` dentro.
2. Abre `VoiceOFF.html` con Chrome o Edge.
3. **Biblioteca → Importar carpeta…** y elige la carpeta.

En segundos queda todo instalado.

> ⚠️ **Importante:** si borras el **historial o los datos de navegación** de Chrome, también se borran las voces instaladas en la app. Haz una copia **cada vez que instales una voz nueva**.

---

## 13. Atajos de teclado

| Atajo | Acción |
|---|---|
| `Ctrl` + `Enter` | Generar y escuchar |
| `Esc` | Detener o cerrar ventana |
| Doble clic en el valor de un control | Volver al valor por defecto |
| Clic en la onda | Saltar a ese punto del audio |

---

## 14. Consejos para que suene mejor

- **Puntúa bien.** Cada punto es una pausa; las comas también marcan el ritmo. Una frase muy larga sin comas suena atropellada.
- **Separa en párrafos.** Cada salto de línea crea una pausa natural.
- **Escribe los números en letras** cuando importe cómo se lean: «dos mil veintiséis» en vez de «2026», «cincuenta por ciento» en vez de «50 %».
- **Siglas:** escríbelas como se pronuncian. Por ejemplo, «ONU» se lee bien, pero «DVD» mejor como «de uve de».
- **Signos de exclamación e interrogación:** úsalos completos (`¡…!` y `¿…?`). La voz cambia la entonación.
- **Para publicidad:** emoción **Alegre**, música **Corporativa** o **Alegre**, ducking alto (60–70 %).
- **Para narración o audiolibro:** emoción **Cálido** o **Neutral**, pausa entre 450 y 600 ms, música **Relax** muy baja o sin música.
- **Para noticias:** emoción **Noticia**, sin reverberación y música baja.

---

## 15. Problemas frecuentes

| Problema | Solución |
|---|---|
| **«Falta instalar el motor de voz»** | Ve a **Biblioteca** e instala el **Motor de voz español**, descargándolo o importando sus 6 archivos. |
| **«Instala al menos una voz española»** | Descarga o importa una voz. Recuerda que cada voz son **2 archivos**: `.onnx` y `.onnx.json`. |
| **La descarga se cortó** | Pulsa **Continuar**: sigue donde quedó. |
| **Hugging Face no abre o da error** | Conecta la VPN o cambia la fuente a **«Espejo (hf-mirror)»**. |
| **Al importar dice «no reconocidos»** | Algún archivo tiene otro nombre. Revisa que se llamen exactamente como en la tabla del [punto 2](#opción-b--sin-internet-desde-archivos). |
| **Las voces desaparecieron** | Se borraron los datos del navegador, o abriste la app con otro navegador. Vuelve a importarlas desde tu copia (**Importar carpeta**). |
| **El MP3 sale como WAV** | Falta el codificador `lame.min.js`. Impórtalo o reinstala el motor. |
| **Con «Sistema» no puedo exportar** | Es normal: el navegador no deja grabar esas voces. Usa **Español offline** para exportar. |
| **La primera frase tarda un poco** | La primera vez de cada sesión la app carga la voz en memoria. Después va rápido. |
| **No me deja elegir carpeta** | Esa función solo existe en **Chrome y Edge**. En otros navegadores usa **Importar archivos** y las descargas normales. |

---

### Créditos y licencias

- Voces: **Piper** (proyecto *rhasspy/piper-voices*). Cada voz tiene su propia licencia abierta, que puedes consultar en su página de Hugging Face.
- Motor: **ONNX Runtime Web** (Microsoft, licencia MIT) y **piper-phonemize** (licencia MIT) con **eSpeak NG** (licencia GPL).
- Codificador MP3: **lamejs** (licencia LGPL).
- Música: generada por la propia app, libre de derechos.

*VoiceOFF Studio — tu estudio de locución, sin depender de internet.*

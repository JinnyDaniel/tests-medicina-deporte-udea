# Tests de campo — Medicina del Deporte (UdeA)

Página web con las proformas de tests de campo (valoración pre-test, PAR-Q, consentimiento informado con firma digital, hoja de registro y cálculo automático), lista para publicar en GitHub Pages.

**Todo funciona dentro del navegador de quien la usa.** No hay servidor, no hay base de datos, no se envía ningún dato a ningún lado — por eso no hace falta configurar nada además de subir los archivos.

Incluye por ahora el **test de caminata de 1 milla (Rockport Walk Test)**, siguiendo el artículo de Kline y cols. (1987), con su lista de chequeo de material/preparación integrada en la propia página. Un "test de laboratorio" queda como "próximamente" en el catálogo, como espacio reservado para el siguiente test que se agregue.

## Archivos de esta carpeta

- `index.html` — catálogo/portada con la lista de tests.
- `milla.html` — el formulario del test de la milla (incluye la lista de chequeo, la valoración, el PAR-Q, el consentimiento y la hoja de registro).
- `jspdf.umd.min.js` — librería para generar los PDF (no requiere internet).
- `mi-logo.png` — tu logo personal (el único logo usado en toda la página y en los PDF).
- `favicon.ico` y `favicon.png` — ícono de la pestaña del navegador.
- `formula-vo2-lmin.png` y `formula-vo2-relativo.png` — las dos ecuaciones de Kline y cols. (1987), tipografiadas en notación matemática (TeX), tal como aparecen en la página junto al formulario.
- `formula-vo2-label.png` y `formula-vo2-label-rel.png` — el símbolo "VO₂máx" en la misma notación matemática, usado junto al resultado (en la página y en el reporte PDF).

No cambies los nombres de estos archivos: el código los busca exactamente con esos nombres.

## Cómo publicarla en GitHub Pages (sin usar la terminal)

1. Entra a [github.com](https://github.com) e inicia sesión (o crea una cuenta gratuita si no tienes).
2. Arriba a la derecha, haz clic en el **+** y elige **New repository**.
3. Ponle un nombre (por ejemplo `tests-medicina-deporte`), déjalo en **Public**, y haz clic en **Create repository**. No marques ninguna otra opción.
4. En la página del repositorio recién creado, haz clic en **Add file → Upload files**.
5. Arrastra los 10 archivos de esta carpeta (`index.html`, `milla.html`, `jspdf.umd.min.js`, `mi-logo.png`, `favicon.ico`, `favicon.png`, `formula-vo2-lmin.png`, `formula-vo2-relativo.png`, `formula-vo2-label.png`, `formula-vo2-label-rel.png`) a la ventana del navegador, o haz clic en "choose your files" y selecciónalos todos a la vez.
6. Baja hasta el final de la página y haz clic en **Commit changes**.
7. Ve a la pestaña **Settings** del repositorio (arriba).
8. En el menú de la izquierda, haz clic en **Pages**.
9. En "Build and deployment", donde dice **Branch**, selecciona `main` y la carpeta `/ (root)`, luego haz clic en **Save**.
10. Espera un minuto y actualiza la página. GitHub te mostrará un enlace como:
    `https://tu-usuario.github.io/tests-medicina-deporte/`

Esa es la dirección pública de tu catálogo de tests. Cualquiera con el enlace puede abrirla y usarla desde su celular o computador, sin instalar nada.

## Cómo actualizar la página más adelante

Cada vez que quieras cambiar algo (agregar un test nuevo, corregir un texto), edita el archivo correspondiente y vuelve a subirlo desde **Add file → Upload files** en el mismo repositorio — GitHub reemplaza el archivo anterior automáticamente y la página publicada se actualiza sola en uno o dos minutos.

## Cómo agregar un nuevo test más adelante

1. Copia `milla.html`, cámbiale el nombre (por ejemplo `veinte-metros.html`) y ajusta el contenido (preguntas, campos, ecuación) siguiendo estrictamente el artículo original de ese test.
2. Agrega una tarjeta nueva en `index.html` que enlace a ese archivo (hay una tarjeta de ejemplo ya deshabilitada — "Test de laboratorio" — que puedes copiar, editar y activar).
3. Sube ambos archivos actualizados igual que en el paso 5 de arriba.

## Nota sobre los PDF descargables

Los botones "Descargar consentimiento informado (PDF)" y "Descargar reporte del test (PDF)" generan el archivo directamente en el navegador de quien esté usando la página — nadie más ve esos datos, ni siquiera tú, a menos que la persona te comparta el PDF descargado. Esto solo funciona correctamente una vez la página esté publicada en GitHub Pages (no al abrir el archivo `milla.html` haciendo doble clic en tu computador).

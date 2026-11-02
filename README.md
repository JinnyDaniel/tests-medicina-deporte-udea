# Tests de campo — Medicina del Deporte (UdeA)

Página web con las proformas de tests de campo de Medicina del Deporte y la Actividad Física: valoración pre-test, PAR-Q, consentimiento informado con firma digital, hoja de registro y cálculo automático del resultado.

**Todo funciona dentro del navegador de quien la usa.** No hay servidor ni base de datos: ningún dato ingresado se envía ni se almacena en ningún lugar. La información solo existe en pantalla mientras dura la prueba, y la única copia que queda es el PDF que se descarga al finalizar.

## Tests incluidos

**Test de caminata de 1 milla (Rockport Walk Test)**, siguiendo el artículo de Kline y cols. (1987) para la estimación del VO₂máx, y la fórmula de Tanaka, Monahan & Seals (2001) para la FC máxima estimada (208 − 0,7 × edad). 
**Test de Bruce en cinta ergométrica (laboratorio)**, siguiendo el artículo de Bruce, Kusumi y Hosmer (1973, *Am Heart J* 85(4):546-62): protocolo multiestadio de 7 estadios de 3 minutos, estimación del VO₂máx por la duración total (ecuación 7, personas sanas: 6,70 − 2,82 × sexo + 0,056 × duración en segundos; sexo 1 = hombre, 2 = mujer), campo opcional de VO₂máx directo (ergoespirometría) y deterioro aeróbico funcional (FAI, ecuaciones 1 y 3 a 6). No incluye la ecuación 8 (hombres con enfermedad cardiovascular).

El formulario incluye:

- Lista de chequeo de material y preparación, tanto para el examinador como para el participante.
- Valoración pre-test (datos del participante, antecedentes, signos vitales basales) y PAR-Q.
- Consentimiento informado con firma digital del participante.
- Firma digital y registro médico (RM) del examinador: quien use el formulario dibuja su propia firma y escribe su RM, que quedan junto a los del participante en ambos documentos. No hay ninguna firma precargada: cada examinador firma con la suya.
- Cálculo automático del VO₂máx (en L/min y en ml·kg⁻¹·min⁻¹) a partir de peso, edad, sexo, tiempo de caminata y frecuencia cardíaca del último cuarto de milla.
- Generación de dos documentos en PDF: el consentimiento informado firmado y el reporte completo del test, con el nombre del paciente incluido automáticamente en el nombre del archivo descargado.

## Archivos del proyecto

- `index.html` — catálogo/portada con la lista de tests.
- `milla.html` — el formulario del test de la milla (lista de chequeo, valoración, PAR-Q, consentimiento y hoja de registro).
- `bruce.html` — el formulario del test de Bruce (misma estructura; la hoja de registro es una tabla por estadios con FC, TA, Borg y ECG/síntomas, más 5 minutos de recuperación).
- `jspdf.umd.min.js` — librería para generar los PDF (no requiere internet).
- `logo-header.png` — logo a color, usado en la cabecera de la página (catálogo y formulario).
- `logo-pdf.png` — logo en versión monocromática, usado en la barra lateral de los PDF (reporte y consentimiento).
- `favicon.ico` y `favicon.png` — ícono de la pestaña del navegador (insignia circular del logo).
- `formula-vo2-lmin.png` y `formula-vo2-relativo.png` — las dos ecuaciones de Kline y cols. (1987), tipografiadas en notación matemática (TeX), tal como aparecen en la página junto al formulario.
- `formula-bruce-vo2.png`, `formula-bruce-fai.png` y `formula-bruce-pred.png` — las ecuaciones 7, 1 y 3 a 6 de Bruce y cols. (1973), tipografiadas en TeX (KaTeX) con el mismo estilo que las de la milla.
- `foto-autor.jpg` — foto usada en la sección "Acerca del autor" del catálogo.

El código hace referencia a estos archivos por su nombre exacto, así que no deben renombrarse.

## Nota sobre los PDF descargables

Los botones "Descargar consentimiento informado (PDF)" y "Descargar reporte del test (PDF)" generan el archivo directamente en el navegador de quien esté usando la página — nadie más ve esos datos, ni siquiera el examinador, a menos que la persona comparta el PDF descargado. El nombre del archivo incluye automáticamente el nombre del paciente (por ejemplo `reporte_test_milla_Juan_Perez.pdf`), sin tildes ni caracteres especiales, para facilitar su identificación y archivo. Esta generación de PDF requiere que la página se sirva desde un servidor web (no al abrir `milla.html` haciendo doble clic directamente en el computador).

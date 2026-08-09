# Herramienta NO OFICIAL de Apoyo a HEARTS en el Primer Nivel de Atención

## Propósito
Esta herramienta fue desarrollada de manera independiente para reducir la carga cognitiva y disminuir la inercia terapéutica del personal de salud en los puestos y centros de atención primaria (CAP). Su objetivo es facilitar el cálculo de riesgos, la estratificación de metas y el escalonamiento farmacológico en el manejo de enfermedades crónicas (HTA y DM2), traduciendo los algoritmos teóricos en acciones clínicas inmediatas y seguras.

## Alcance
* **Qué HACE:** Clasifica el nivel de riesgo cardiovascular (RCV), evalúa si un paciente crónico estable está en metas de control, sugiere el siguiente paso en el algoritmo de tratamiento (intensificación o desescalonamiento) y automatiza el cálculo logístico de requisición de farmacia.
* **Qué NO hace:** No diagnostica patologías agudas, no sustituye la valoración médica presencial, y no está diseñada para el manejo de pacientes inestables, hospitalizados o en salas de emergencia.

## Fuentes
Los algoritmos lógicos y las metas terapéuticas programadas en esta herramienta están basados estrictamente en la **Vía Clínica MSPAS/HEARTS Guatemala (Versión vigente a la fecha de creación)** y las **Tablas de Estratificación de Riesgo Cardiovascular no basadas en laboratorio de la OMS/OPS**.

## Fecha de Última Revisión
**Agosto 2026.** 
*⚠️ Si la Vía Clínica Nacional ha sufrido actualizaciones posteriores a esta fecha, esta herramienta debe considerarse obsoleta hasta que su código sea revisado y adaptado.*

## Limitaciones
Esta herramienta **NO** debe utilizarse y carece de validez clínica en los siguientes escenarios:
* Pacientes mujeres embarazadas o en periodo de lactancia.
* Menores de 18 años.
* Pacientes con emergencias hipertensivas (≥180/120 mmHg con signos de daño a órgano blanco).
* Pacientes con emergencias metabólicas (hipoglucemias severas, cetoacidosis, estado hiperosmolar).
* Pacientes con dolor torácico, déficit neurológico agudo o sospecha de lesión renal aguda.

## Medicamentos (Factibilidad Operativa)
¿Por qué esta herramienta utiliza únicamente un listado reducido de medicamentos (Metformina, Glimepirida, Gliclazida, Canagliflozina, Irbesartán, Enalapril, Amlodipino, Hidroclorotiazida y Atorvastatina)?
La aplicación está adaptada a la **disponibilidad real y factible de medicamentos** observada en los establecimientos del primer nivel de atención del MSPAS, específicamente en el departamento de Quiché, en los municipios de Chichicastenango, Canillá, Chinique, Zacualpa y Joyabaj. No pretende reproducir el listado internacional completo de fármacos sugeridos por HEARTS global, sino ofrecer soluciones viables con el inventario existente en el terreno.

## Filosofía de Diseño
El diseño de la interfaz reconoce la frontera crítica entre *lo que el protocolo espera que haga el trabajador* y *lo que el trabajador razonablemente puede ejecutar durante una jornada real saturada*. Por ejemplo, se incluye la opción de evaluar la presión arterial con una "medición única orientativa", reconociendo que exigir siempre 4 mediciones espaciadas en un puesto de salud colapsado puede llevar al abandono de la herramienta. El objetivo es cerrar la brecha operativa, prefiriendo una aproximación estructurada y segura a la inercia terapéutica total.

## Advertencia Legal e Institucional
**HERRAMIENTA NO OFICIAL.** Este software no es un instrumento oficial del Ministerio de Salud Pública y Asistencia Social (MSPAS), la OPS/OMS ni de ninguna otra institución gubernamental o no gubernamental. Su finalidad es estrictamente de apoyo operativo. **No sustituye la normativa vigente, la valoración profesional ni los protocolos institucionales. En caso de discrepancia entre las recomendaciones de esta herramienta y la normativa oficial vigente, prevalece siempre la normativa oficial.**

## Cómo Modificarla (Para futuros mantenedores)
Si el desarrollador original ya no participa en el mantenimiento de este proyecto y las guías clínicas han cambiado, el código fuente es completamente abierto y modificable.
* La lógica está escrita en HTML, CSS y JavaScript básico (sin frameworks complejos) para asegurar su durabilidad y fácil edición.
* Para modificar metas de presión arterial o dosis: Edite el archivo `Herramienta_HTA.html` buscando la función `evaluarMetas()` y `calcularTratamiento()`.
* Para modificar algoritmos de glucosa: Edite el archivo `Herramienta_DM2.html` buscando la función `obtenerEstadoDx()`.
* Para actualizar las tablas de riesgo: Edite la matriz `matrizRiesgo` dentro de `Calculadora_RCV.html`.

*El código vive en internet para quien desee multiplicarlo y continuar el servicio.*

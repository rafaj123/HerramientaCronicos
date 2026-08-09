# Herramienta Crónicos — Memoria Técnica v1.0

**Autor:** Dr. Rafael Antonio Juárez Vargas  
**Fecha:** Agosto 2026  
**Ámbito:** Primer Nivel de Atención — Quiché, Guatemala  
**Repositorio:** [github.com/rafaj123/HerramientaCronicos](https://github.com/rafaj123/HerramientaCronicos)

---

## Propósito y Problema Identificado
Esta herramienta fue desarrollada de manera independiente para reducir la carga cognitiva y disminuir la inercia terapéutica del personal de salud en los puestos de salud y centros de atención primaria (CAP) del primer nivel. Su objetivo es facilitar la clasificación de riesgo, la estratificación de metas y el escalonamiento farmacológico en el manejo de enfermedades crónicas (Hipertensión Arterial y Diabetes Mellitus Tipo 2), traduciendo los algoritmos teóricos en acciones clínicas inmediatas, estructuradas y seguras.

## Alcance
* **Qué HACE:** Clasifica el nivel de riesgo cardiovascular (RCV), evalúa si un paciente crónico estable está en metas de control, sugiere el siguiente paso en el algoritmo de tratamiento (intensificación o desescalonamiento), detecta alertas de seguridad/efectos adversos y automatiza el cálculo logístico de requisición de farmacia.
* **Qué NO HACE:** No diagnostica patologías agudas, no sustituye la valoración médica presencial, y no está diseñada para el manejo de pacientes inestables, hospitalizados o en salas de emergencia.

## Población Objetivo
* **Usuarios primarios:** Médicos en ejercicio (EPS), Médicos generales y personal de enfermería y auxiliares de salud del primer y segundo nivel de atención.
* **Beneficiarios:** Pacientes adultos con riesgo cardiovascular, hipertensión arterial y diabetes mellitus tipo 2.

## Fuentes Clínicas y Normativas
Los algoritmos lógicos, las metas terapéuticas y los esquemas de tratamiento programados en esta herramienta están basados estrictamente en:
* **Vía Clínica MSPAS/HEARTS Guatemala (versión 2026).**
* **HEARTS 2.0** y directrices de la **American Heart Association (AHA)**.
* **Tablas de Estratificación de Riesgo Cardiovascular no basadas en laboratorio de la OMS/OPS (Región de las Américas).**
* Criterios de la *American Diabetes Association* (ADA) 2026 para metas de HbA1c e individualización de tratamiento.

## Fecha de Última Revisión
**Agosto 2026.**  
*⚠️ Si la Vía Clínica Nacional o las guías de referencia sufren actualizaciones posteriores a esta fecha, esta herramienta debe considerarse obsoleta hasta que su código sea revisado y adaptado.*

## Limitaciones y Exclusiones
Esta herramienta **NO** debe utilizarse y carece de validez clínica en los siguientes escenarios:
* Pacientes mujeres embarazadas, en periodo de lactancia o en búsqueda activa de embarazo.
* Menores de 18 años.
* Pacientes con emergencias hipertensivas (PA ≥180/120 mmHg con signos de daño a órgano blanco).
* Pacientes con emergencias metabólicas (hipoglucemias severas, cetoacidosis, estado hiperosmolar).
* Pacientes con dolor torácico, déficit neurológico agudo, sospecha de sepsis o lesión renal aguda.

## Medicamentos (Factibilidad Operativa)
¿Por qué esta herramienta utiliza un listado reducido de medicamentos (Metformina, Glimepirida, Gliclazida, Canagliflozina, Irbesartán, Enalapril, Amlodipino, Hidroclorotiazida y Atorvastatina)?  
La aplicación está adaptada a la **disponibilidad real y factible de medicamentos** observada en los establecimientos del primer nivel de atención del MSPAS, específicamente en el departamento de Quiché (en municipios como Chichicastenango, Canillá, Chinique, Zacualpa, Joyabaj, entre otros). No pretende reproducir el listado internacional completo de fármacos sugeridos por HEARTS global, sino ofrecer soluciones viables y prescripciones seguras con el inventario existente en el terreno.

## Filosofía de Diseño y Telemetría
El diseño de la interfaz reconoce la frontera crítica entre *lo que el protocolo espera que haga el trabajador* y *lo que el trabajador razonablemente puede ejecutar durante una jornada real saturada*. Por ejemplo, se incluye la opción de evaluar la presión arterial con una "medición única orientativa", reconociendo que exigir siempre 4 mediciones espaciadas en un puesto de salud colapsado puede llevar al abandono de la herramienta.

Asimismo, la suite integra un canal de **telemetría anónima y silenciosa** (vía *Webhooks* en la sombra) que permite recolectar datos sobre la adopción de la herramienta, alertas de seguridad prevenidas e inercia terapéutica por distrito, garantizando en todo momento un diseño *HIPAA-compliant* sin almacenamiento de datos personales de pacientes.

## Advertencia Legal e Institucional (Disclaimer)
**HERRAMIENTA NO OFICIAL.** Este software es un instrumento **independiente y no oficial** de apoyo a la toma de decisiones clínicas. No es un producto del Ministerio de Salud Pública y Asistencia Social (MSPAS), la OPS/OMS, la AHA ni de ninguna otra institución gubernamental o no gubernamental. Su finalidad es estrictamente de apoyo operativo y educativo. **No sustituye la normativa vigente, la valoración profesional ni los protocolos institucionales. En caso de discrepancia entre las recomendaciones de esta herramienta y la normativa oficial vigente, prevalece siempre la normativa oficial del MSPAS.**

## Cómo Modificarla (Para futuros mantenedores)
Si las guías clínicas cambian o deseas adaptar la herramienta a otras regiones, el código fuente es completamente abierto y auditable:
* La lógica está escrita en HTML, CSS y JavaScript vainilla (sin frameworks complejos) para asegurar durabilidad y fácil edición.
* **Presión Arterial y Metas:** Edite `Herramienta_HTA.html` buscando las funciones `evaluarMetas()` y `calcularTratamiento()`.
* **Algoritmos de Glucosa:** Edite `Herramienta_DM2.html` buscando la función `obtenerEstadoDx()` y `evaluarTratamiento()`.
* **Tablas de Riesgo Cardiovascular:** Edite la matriz `matrizRiesgo` en `Calculadora_RCV.html`.

*El código vive en internet para quien desee multiplicarlo y continuar el servicio.*

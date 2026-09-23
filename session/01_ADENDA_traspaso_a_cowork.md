# Adenda al brief de traspaso — estado al 9 de septiembre de 2026

Complemento de `00_BRIEF_traspaso_proyecto.md`. No lo reemplaza. Recoge lo decidido
y lo producido después de su redacción. Leer los dos juntos.

---

## 1. Hechos nuevos que invalidan partes del brief

**El correo al DAAD se envió** (8 de septiembre), como respuesta al hilo de Hanna
Cornelius y Elif Keles, con copia a Andrea Cardoso. Cubre cuatro puntos: no asistencia
a la excursión del Futurium ni a las demás sesiones del jueves por la mañana más
solicitud de hora de acceso y sala asignada; rol de Andrea; corrección de la
descripción del booklet remitiendo al texto ya enviado en la encuesta de sesión;
y requisitos técnicos (dispositivos de los participantes, disposición de mesas,
proyector y tomas, conectividad, número de inscritos y centros de origen).
**Sin respuesta al momento de escribir esto.**

**Los cupos del WS 4 están llenos.** El correo del DAAD del 7 de septiembre lo dice
dos veces. Queda sin efecto todo el razonamiento del brief sobre el riesgo de no
alcanzar los ocho inscritos mínimos.

**Parte de la sala fue asignada, no eligió.** Los participantes se distribuyeron por
rol y por preferencias de registro, y el DAAD pide expresamente que acepten su
asignación. Consecuencia de diseño: no se puede presumir motivación de entrada.

**Los doctorandos no estarán.** El PhD Retreat Part 3 corre en paralelo (13:30–17:30).
La sala será profesorado, coordinadores de centro y profesionales. Registro de pares.

**El horario está confirmado en la rejilla oficial: 13:30 a 15:30 exactas.** El almuerzo
va de 12:15 a 13:30, setenta y cinco minutos. Los talleres vecinos duran cuatro y cinco
horas; el de Víctor es el más corto de la tarde.

**El miércoles 30 a las 15:30 hay una plenaria titulada "From Santa Marta to the Global
Stage: Scaling the Science-Policy Nexus to Phase Out Fossil Fuels".** Gancho de apertura
disponible para el jueves. Conviene asistir tomando nota.

**El martes 29 por la mañana Víctor está inscrito en el WS 2** ("Whose Land, Whose Trees,
Whose Rules?"), taller del mismo género. Oportunidad de observar facilitación y de
identificar a quién tendrá el jueves.

**Viaje el 25 de septiembre.** El congelamiento se adelanta al **21 de septiembre**.

---

## 2. Decisiones cerradas en este hilo

- **Facilitación en solitario.** Andrea Cardoso asiste como apoyo, sin bloques asignados.
  Puede circular por la mesa que Víctor no esté atendiendo.
- **Dos mesas de cuatro**, con ramas de contingencia si llegan más personas.
- **Sesión digital con respaldo impreso.** Portátiles o tabletas de los participantes,
  un dispositivo por mesa como mínimo. Víctor lleva dos equipos propios con la herramienta
  en USB, independientemente de lo que responda el DAAD.
- **El SIG es un panel permanente**, no una vista final. Va en la columna derecha de la
  herramienta, entre el selector de tecnología y la tabla de ranking, alimentado por la
  misma llamada a `draw()`.
- **`gMin` se queda en 0,15.** Lo que hay que corregir es `CORRECCIONES_pendientes.md`,
  que pide 0,30. Justificación en la sección 4.
- **Escala departamental, no sub-departamental.** El INC y el ING existen solo a nivel
  de departamento; por debajo no hay con qué cruzar las áreas viables.
- **Dibujo en SVG en línea, sin librería de mapas y sin capa base.** Coherente con la
  promesa de funcionamiento sin conexión hecha al DAAD por escrito.

---

## 3. Flujo de sesión ajustado

Conserva el arco propuesto por Víctor y la arquitectura cerrada de 30/50/40, con
tres correcciones: el SIG se adelanta a las fases 1 y 2, los escenarios los producen
las mesas en lugar de construirse en vivo, y se reinserta la bisagra conceptual.

1. Territorio primero: el mapa base en pantalla antes de explicar el método.
2. El método, y por qué el INC y el ING quedaron fuera del álgebra.
3. Cada mesa pondera con BWM y ve recalcularse su propio mapa. Aquí ya es SIG-MCDM.
4. La bisagra: cada mesa decide dónde va el conflicto y anota qué no captura su
   indicador. El mapa cambia a la vista.
5. Los dos mapas lado a lado, y el cierre escrito por las mesas y exportado por la
   herramienta.

Principio rector derivado de facilitar en solitario: **la sesión se documenta sola.**
Instrucciones impresas por mesa en vez de habladas, un relator nombrado por mesa desde
el primer minuto, plantilla en la que se escribe el entregable final y no notas para
pasar en limpio, y exportación desde la herramienta.

---

## 4. Verificación de la herramienta

Contrastada contra las siete correcciones pendientes. **Las correcciones 1, 2, 3, 4, 5
y 7 ya estaban aplicadas.** El pendiente 1 del brief (valores departamentales de INC e
ING) está obsoleto: los valores reales están cargados.

De la corrección 6 está aplicado todo salvo `gMin`. Verificación aritmética del
escalonamiento con `tMid` en 0,10: tres departamentos en el primer nivel, cinco en el
segundo y cuatro en el tercero, exactamente lo que la corrección anticipaba.

**Sobre `gMin`.** Con `cMax` en 0,08, seis de los doce departamentos con eólica salen
por conflictividad. Los seis restantes forman una escalera de gobernanza casi regular:
Cesar 0,118 · Atlántico 0,162 · Cundinamarca 0,211 · Tolima 0,285 · Magdalena 0,420 ·
Boyacá 0,463. Con paso de deslizador de 0,05, cada tirón entre 0,10 y 0,30 excluye
exactamente un departamento.

| `gMin` | Excluidos | Sobreviven |
|---|---|---|
| 0,10 | 6 de 12 | 6 |
| **0,15** | **7 de 12** | **5** |
| 0,20 | 8 de 12 | 4 |
| 0,25 | 9 de 12 | 3 |
| 0,30 | 10 de 12 | 2 |
| 0,50 | 12 de 12 | 0 |

0,15 deja el criterio visiblemente activo en el valor por defecto, conserva toda la
escalera hacia arriba y un escalón hacia abajo, y mantiene cinco sobrevivientes legibles.
Con 0,30 quedan dos y el modo deja de demostrar nada.

**Momento demostrativo para el guion:** arrastrar de 0,15 a 0,30 en eólica excluye tres
departamentos uno por uno; hacer lo mismo en solar no produce nada entre 0,20 y 0,25 y
luego bota cuatro de golpe en 0,30. El mismo umbral se comporta distinto según el
recurso, y ese contraste es en sí mismo un argumento sobre lo arbitrario de fijar
umbrales de gobernanza.

**El apartado de método ya existe** dentro de la herramienta, bilingüe, con ancla de
navegación propia. Cubre las dos vías separadas, la normalización, BWM frente a CRITIC,
y por qué la ubicación del conflicto es una decisión de gobernanza. No hace falta añadir
nada ahí.

---

## 5. Artefactos producidos en este hilo

| Archivo | Qué es |
|---|---|
| `gente-decision-tool-v3.html` | Herramienta con los cinco logos embebidos en base64. 227 KB. Sin dependencias externas |
| `col_departamentos.geojson` | 32 departamentos, 3.311 vértices, 56 KB. Fuente Natural Earth, dominio público. Los 17 departamentos con datos GENTE coinciden por nombre exacto con el arreglo `DEP`, sin excepciones |

Los logos (Unimagdalena, TRAJECTS, MAGMA, ANH y Semillero de Transición Energética)
quedaron con el fondo recortado por relleno desde los bordes, no por color, para no
perforar los blancos internos del emblema de la ANH. TRAJECTS va a 62 px por ser un
logo vertical; los demás entre 38 y 46 px, equilibrio óptico y no igualdad matemática.

**Aviso:** el arte original del logo de MAGMA dice "GRUPD DE INVESTIGACIÓN", con D en
lugar de O. A 40 px no se nota, pero el mismo archivo en pósteres sí lo mostraría.

---

## 6. Calendario

| Fechas | Trabajo |
|---|---|
| 8–13 sept | Capa SIG sobre la herramienta |
| 14–17 sept | Guion v2.0 en solitario, dos mesas |
| 18–20 sept | Plantilla autodocumentada, tarjetas de mesa, exportación |
| 21 sept | Dos ensayos cronometrados y **congelamiento** |
| 22–24 sept | Impresión del respaldo y empaque |
| 25 sept | Viaje |

---

## 7. Obsolescencias detectadas en el guion v1.0

- El bloque 1 dice literalmente *Thank you for choosing this room*. Falso: parte de la
  sala fue asignada. Reescribir.
- El mismo bloque presenta a Andrea como co-facilitadora. Ahora es apoyo.
- Los bloques 9, 15, 26, 27, 28 y 30 estaban asignados a Andrea (24 de 120 minutos).
  Absorberlos sin más llevaría a Víctor cerca del 40 % del tiempo de habla, y los
  bloques 26 a 28 son físicamente imposibles en solitario: son trece minutos de
  transcribir en vivo mientras se hacen las preguntas que generan lo transcrito.
- El montaje asume papel: mapas A2 desplegados, fichas boca abajo, separatas por silla.

---

## 8. Pendientes vivos

1. Respuesta del DAAD al correo del 8 de septiembre.
2. Construcción de la capa SIG. Sin empezar.
3. Guion v2.0. Sin empezar.
4. Plantilla autodocumentada y tarjetas de instrucción por mesa. Sin empezar.
5. Exportación desde la herramienta. Sin empezar.
6. Figuras cartográficas publicadas de GENTE (eólica y solar) para el respaldo impreso
   y para igualar la escala cromática de la pantalla con el papel.
7. Corregir `gMin` a 0,15 en `CORRECCIONES_pendientes.md`.
8. Decidir si el logo del Semillero se queda en la tira. El brief autoriza cuatro
   logos; hay cinco.
9. Correo aparte al DAAD por el error de fechas del hotel del Infokit ("9–13 September
   2024") y por la extensión de estadía.

---

## 9. Restricciones vigentes, sin cambios

- El manuscrito de *Heliyon* está en revisión: se proyecta rotulado *under review*,
  no se distribuye. El de *Land* está en CC BY: se imprime y se reparte con DOI.
- Todo producto derivado atribuye al proyecto GENTE, desarrollado por la Universidad
  del Magdalena para la ANH bajo el Contrato 618 de 2025.
- No usar el logo del DAAD sin autorización explícita.
- La herramienta debe funcionar sin conexión. Comprometido por escrito ante el DAAD
  en el correo del 8 de septiembre.

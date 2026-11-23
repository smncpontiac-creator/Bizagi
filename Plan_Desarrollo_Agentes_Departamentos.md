# Plan de Desarrollo: Agentes y Departamentos para una Cadena de Suministro Sustentable

**Empresa:** Buzines (confección y bordado textil)
**Asignatura:** Logística Circular y Sustentabilidad. Situación de Evaluación N°3 (Rúbrica 25 %)
**Base del trabajo:** diagnóstico AS-IS ya desarrollado en la asignatura:

- `proceso_buzines_lean.bpmn`: proceso actual con 6 departamentos y 12 mudas (M1–M12).
- `Bodega_Textiles_FlexSim_Model.fsc`: simulación de la bodega de 25 × 15 × 5 m.
- `plan_desarrollo_sustentable_TOBE.bpmn` (**nuevo**): proceso TO-BE, donde cada *pool* es un **departamento** y cada *lane* es un **agente** responsable.

---

## 1. Introducción

En el diagnóstico Lean se identificaron 12 puntos críticos (mudas) en la cadena de suministro de Buzines. Su impacto económico estimado es de **$24–38 M/año**. Seis de ellos son críticos: transporte innecesario, defectos de confección, búsqueda de materiales, control de calidad redundante, captura triplicada de datos y manejo de inventario en Excel.

Este plan define los **departamentos** y **agentes** que hacen falta para ejecutar el plan de acción y quién responde por cada meta, KPI y política. Se mantienen los departamentos actuales y se crean tres nuevos. Así se cubren los eslabones que hoy no tienen dueño: abastecimiento sustentable, logística inversa y gobierno de la sustentabilidad.

## 2. Objetivos

**General:** organizar la estructura de departamentos y agentes de Buzines para transformar su cadena de suministro en una cadena sustentable y circular, con mejora continua.

**Específicos:**
1. Definir lineamientos estratégicos de sustentabilidad para la cadena (criterio 3.1.1).
2. Asignar metas por eslabón y un agente responsable para cada una (3.1.2).
3. Establecer KPI para los eslabones de mayor impacto (3.1.3).
4. Distribuir las tareas del equipo y ajustarlas según el cumplimiento de las metas (3.1.4).
5. Formular políticas de sustentabilidad ligadas a la mejora continua (3.1.5).

## 3. Materiales y métodos

- **Mapeo de procesos BPMN 2.0 en Bizagi Modeler:** modelo AS-IS (diagnóstico) y modelo TO-BE (este plan).
- **Lean Manufacturing:** identificación de las 7+1 mudas, 5S, Kanban, Jidoka, Poka-Yoke y células de manufactura.
- **Simulación FlexSim:** layout de la bodega, racks y flujos de picking.
- **Matriz de riesgo:** Probabilidad (1–5) × Impacto (1–5).
- **Matriz RACI:** asignación de responsabilidades por departamento y agente.
- **Ciclo PDCA:** revisión mensual de los KPI en el Comité de Sustentabilidad.

---

## 4. Resultados

### 4.1 Lineamientos estratégicos (3.1.1)

| # | Lineamiento | Principio de sustentabilidad |
|---|---|---|
| L1 | Eliminar desperdicios de proceso (mudas) y de material | Eficiencia en el uso de recursos |
| L2 | Reducir emisiones del transporte interno y de distribución | Ambiental (huella de carbono) |
| L3 | Comprar a proveedores evaluados con criterios ambientales y sociales (ESG) | Responsabilidad en la cadena |
| L4 | Cerrar el ciclo del textil: retazos, mermas y prendas en fin de vida | Economía circular |
| L5 | Usar un único sistema de datos (ERP-WMS) y decidir con KPI | Gestión basada en evidencia |
| L6 | Mejorar continuamente con participación de todas las personas | Social y mejora continua |

### 4.2 Departamentos y agentes del plan

Estos son los pools y lanes del archivo `plan_desarrollo_sustentable_TOBE.bpmn`.

| Departamento (pool) | Estado | Agentes (lanes) | Rol en la cadena sustentable | Mudas que resuelve |
|---|---|---|---|---|
| **Cliente** (externo) | Existente | Cliente / comprador corporativo | Aprueba con checklist objetivo y devuelve prendas en fin de vida | M1, M2 |
| **Ventas y Atención al Cliente** | Existente | Ejecutivo comercial | Registra en CRM, cotiza alternativas sustentables y completa un brief estandarizado | M11 |
| **Diseño y Bordado** | Existente | Diseñador gráfico; Técnico de bordado | Trabaja con banco de referencias y entrega una ficha técnica digital que reduce reprocesos | M1, M2, M11 |
| **Administración y Finanzas** | Existente (reforzado) | Encargado ERP-WMS; **Analista de datos y KPI [nuevo]** | Mantiene el registro único de datos, la facturación electrónica y el tablero de KPI | M5, M12 |
| **Abastecimiento y Compras Sustentables** | **NUEVO** | Comprador / Gestor de proveedores | Repone por Kanban, evalúa proveedores con criterios ESG y emite OC verdes | M6 |
| **Proveedores certificados** (externo) | Nuevo actor | Proveedor de telas e insumos | Entrega material certificado (reciclado/orgánico) en embalaje retornable | — |
| **Producción** | Existente (reorganizado) | Jefe de producción; Operario de confección (célula); **Inspector de calidad Jidoka** | Trabaja en células con SOP, 5S y Poka-Yoke, y controla la calidad en línea | M8, M9, M10 |
| **Bodega y Logística** | Existente (reforzado) | Jefe de bodega (WMS); Operario de bodega/picking; Conductor | Usa código de barras y ubicaciones fijas, prepara kits, hace picking por olas y despacho consolidado | M3, M4, M5, M7 |
| **Logística Inversa y Gestión de Residuos** | **NUEVO** | Encargado de economía circular; Gestor externo de residuos | Clasifica retazos por fibra, recibe devoluciones y valoriza/recicla con certificado | Residuos (L4) |
| **Gerencia y Comité de Sustentabilidad** | **NUEVO** | Coordinador de sustentabilidad y mejora continua; Gerente general | Revisa KPI y la matriz de riesgo (PDCA), ajusta el plan y aprueba políticas | Gobierno del plan |

**Resumen:** 10 departamentos (7 internos, 2 externos y el cliente) y 18 agentes. Se crean **3 departamentos nuevos** y **3 agentes nuevos o redefinidos**: Analista de KPI, Inspector Jidoka y Coordinador de sustentabilidad.

#### Perfil de los agentes nuevos

| Agente | Departamento | Funciones principales | Dedicación sugerida |
|---|---|---|---|
| Coordinador de sustentabilidad y mejora continua | Comité de Sustentabilidad | Liderar el PDCA mensual, actualizar la matriz de riesgo, redactar políticas y capacitar en 5S/Lean | 1 persona (puede ser jornada parcial al inicio) |
| Analista de datos y KPI | Administración y Finanzas | Mantener el tablero de KPI, validar los datos del ERP-WMS y alertar desviaciones | 1 persona o función asignada al Encargado ERP |
| Comprador / Gestor de proveedores | Abastecimiento | Kanban de insumos, evaluación ESG de proveedores y negociación de embalaje retornable | 1 persona |
| Encargado de economía circular | Logística Inversa | Clasificar mermas, gestionar el programa de retorno de prendas y coordinar con el gestor externo | Función compartida con Bodega al inicio |
| Inspector de calidad Jidoka | Producción | Detener la línea ante defectos, registrar causas raíz y eliminar la inspección redundante final | Rol rotativo entre operarios capacitados |

### 4.3 Matriz de riesgo de los puntos críticos

Escala: Probabilidad (P) e Impacto (I) de 1 a 5. Nivel = P × I. **Crítico** ≥ 20, **Alto** 12–19, **Medio** 6–11.

| Punto crítico (diagnóstico) | Eslabón | P | I | Nivel | Prioridad | Agente responsable |
|---|---|---|---|---|---|---|
| M4 Transporte innecesario bodega-matriz ($6,6 M/año; ~660 viajes/año) | Logística interna | 5 | 5 | 25 | **Crítico** | Jefe de producción + Jefe de bodega |
| M9 Defectos de confección / layout ($5,5–8,5 M/año) | Producción | 4 | 5 | 20 | **Crítico** | Jefe de producción |
| M3 Búsqueda de materiales ($2,75–3,62 M/año) | Almacenamiento | 5 | 4 | 20 | **Crítico** | Jefe de bodega |
| M12 Captura triplicada ERP + Excel + papel ($1–2 M/año) | Información | 5 | 3 | 15 | Alto | Encargado ERP-WMS |
| M5 Inventario en Excel, 15–25 % de errores ($0,8–1,2 M/año) | Almacenamiento | 5 | 3 | 15 | Alto | Jefe de bodega |
| M10 Inspecciones redundantes ($2–4 M/año) | Producción | 4 | 4 | 16 | Alto | Inspector Jidoka |
| M2 Muestras con 30 % de ajustes ($2–4 M/año) | Desarrollo de producto | 4 | 4 | 16 | Alto | Técnico de bordado |
| M6 Inventario excesivo clase C ($15–30 M inmovilizados) | Abastecimiento | 3 | 4 | 12 | Alto | Comprador |
| M8 Reproceso de muestras ($1,5–2,5 M/año) | Producción | 4 | 3 | 12 | Alto | Operario de confección |
| R-S1 Retazos y mermas sin gestión (va a relleno sanitario) | Fin de vida | 4 | 3 | 12 | Alto | Encargado de economía circular |
| R-S2 Proveedores sin trazabilidad ambiental | Abastecimiento | 3 | 3 | 9 | Medio | Comprador |
| M1 Espera de aprobación del cliente (3–7 días) | Cliente / Ventas | 4 | 2 | 8 | Medio | Ejecutivo comercial |
| M7 Picking sin ruta / coordinación telefónica ($0,4–0,7 M/año) | Distribución | 3 | 2 | 6 | Medio | Operario de bodega |
| M11 Brief incompleto (retraso de 3–5 días) | Diseño | 3 | 2 | 6 | Medio | Diseñador |

### 4.4 Plan de acción por plazo y agente responsable

| Plazo | Acción | Riesgo que mitiga | Departamento | Agente responsable |
|---|---|---|---|---|
| **Corto (0–6 meses)** | 5S y ubicaciones fijas con código de barras en la bodega (layout FlexSim) | M3, M5 | Bodega y Logística | Jefe de bodega |
| Corto | Kitting: kit de materiales por orden de producción | M3, M8 | Bodega y Logística | Operario de bodega |
| Corto | Brief estandarizado y checklist de aprobación para el cliente | M1, M11 | Ventas / Diseño | Ejecutivo comercial / Diseñador |
| Corto | Ficha técnica digital para muestras | M2, M8 | Diseño y Bordado | Técnico de bordado |
| Corto | Separación de retazos por tipo de fibra en el puesto de trabajo | R-S1 | Logística Inversa | Encargado de economía circular |
| Corto | Conformar el Comité de Sustentabilidad y nombrar al Coordinador | Gobierno | Gerencia | Gerente general |
| **Mediano (6–18 meses)** | Integración ERP-WMS con registro único de datos | M12, M5 | Administración y Finanzas | Encargado ERP-WMS |
| Mediano | Células de confección con SOP y Poka-Yoke; control Jidoka en línea | M9, M10 | Producción | Jefe de producción / Inspector Jidoka |
| Mediano | Transporte consolidado (1 viaje/día con ruta planificada) | M4 | Producción / Bodega | Jefe de producción / Conductor |
| Mediano | Kanban de insumos y liquidación de inventario clase C | M6 | Abastecimiento | Comprador |
| Mediano | Evaluación ESG de proveedores y embalaje retornable | R-S2 | Abastecimiento | Comprador |
| Mediano | Tablero mensual de KPI | Todos | Administración y Finanzas | Analista de KPI |
| **Largo (18–36 meses)** | Consolidar bodega y matriz en un solo sitio, o WMS multi-sitio | M4 (eliminación definitiva) | Gerencia / Bodega | Gerente general |
| Largo | Programa de retorno de prendas corporativas en fin de vida | R-S1 | Logística Inversa / Ventas | Encargado de economía circular |
| Largo | Convenio con gestor de reciclaje textil y certificado de valorización | R-S1 | Logística Inversa | Gestor externo de residuos |
| Largo | Línea de productos con tela reciclada u orgánica | L3, L4 | Ventas / Abastecimiento | Ejecutivo comercial / Comprador |

### 4.5 Metas por eslabón de la cadena (3.1.2)

| Eslabón | Meta | Plazo | Agente dueño de la meta |
|---|---|---|---|
| Abastecimiento | 80 % de las compras de tela a proveedores evaluados con criterios ESG | 18 meses | Comprador |
| Abastecimiento | Reducir en 40 % el capital inmovilizado en inventario clase C | 12 meses | Comprador |
| Almacenamiento | Bajar el tiempo de búsqueda de material de 15–30 a menos de 5 min por operario al día | 6 meses | Jefe de bodega |
| Almacenamiento | Precisión de inventario ≥ 98 % (hoy los errores son de 15–25 %) | 12 meses | Jefe de bodega |
| Logística interna | Reducir en 60 % los viajes bodega-matriz (de 2–3 a 1 por día) | 12 meses | Jefe de producción |
| Producción | Bajar los defectos de 3–5 % a menos de 1,5 % | 12 meses | Jefe de producción |
| Producción | Reducir las muestras con ajuste de 30 % a menos de 10 % | 6 meses | Técnico de bordado |
| Información | Una sola captura de datos por pedido (de 3 a 1) | 12 meses | Encargado ERP-WMS |
| Distribución | 95 % de entregas a tiempo con despacho consolidado | 12 meses | Conductor / Jefe de bodega |
| Fin de vida | Valorizar ≥ 70 % de los retazos y mermas (desviados del relleno sanitario) | 24 meses | Encargado de economía circular |
| Cliente | Aprobación de diseño en 2 días como máximo (hoy 3–7 días) | 6 meses | Ejecutivo comercial |

### 4.6 Indicadores clave de desempeño (3.1.3)

Los KPI se concentran en los eslabones de mayor impacto según la matriz de riesgo.

| KPI | Fórmula | Línea base | Meta | Frecuencia | Responsable de medir |
|---|---|---|---|---|---|
| Viajes internos por día | N° viajes bodega-matriz / días hábiles | 2–3 | 1 | Semanal | Conductor → Analista KPI |
| Emisiones del transporte interno | km recorridos × factor de emisión (kg CO₂e/km) | ≈ 19.800 km/año* | −60 % | Mensual | Analista KPI |
| Tasa de defectos | Prendas defectuosas / prendas producidas × 100 | 3–5 % | < 1,5 % | Semanal | Inspector Jidoka |
| Muestras con ajuste | Muestras ajustadas / muestras totales × 100 | 30 % | < 10 % | Mensual | Técnico de bordado |
| Tiempo de búsqueda de material | min/operario/día | 15–30 | < 5 | Mensual | Jefe de bodega |
| Exactitud de inventario | Registros correctos / registros auditados × 100 | 75–85 % | ≥ 98 % | Mensual | Jefe de bodega |
| Rotación de inventario clase C | Consumo anual / inventario promedio | Por medir | +50 % | Trimestral | Comprador |
| Compras sustentables | $ compra a proveedores ESG / $ compra total × 100 | 0 % | 80 % | Trimestral | Comprador |
| Tasa de valorización de residuos | kg valorizados / kg de retazos generados × 100 | ≈ 0 % | ≥ 70 % | Mensual | Encargado de economía circular |
| Entregas a tiempo (OTD) | Pedidos a tiempo / pedidos totales × 100 | Por medir | 95 % | Mensual | Jefe de bodega |
| Ahorro acumulado por mudas eliminadas | Σ ahorro por muda vs. línea base | $0 | $16,8–26,6 M/año | Trimestral | Analista KPI |

\* Estimación: 660 viajes/año × 30 km (datos del diagnóstico M4). Se debe validar con registros reales.

### 4.7 Matriz RACI (departamentos × acciones clave)

R = Responsable · A = Aprueba · C = Consultado · I = Informado

| Acción | Comité / Gerencia | Ventas | Diseño | Adm. y Finanzas | Abastecimiento | Producción | Bodega | Log. Inversa |
|---|---|---|---|---|---|---|---|---|
| 5S y código de barras en bodega | A | I | – | C | I | C | **R** | I |
| Integración ERP-WMS | A | C | I | **R** | C | C | C | I |
| Células, SOP y Jidoka | A | – | C | I | I | **R** | C | C |
| Transporte consolidado | A | I | – | I | C | **R** | **R** | – |
| Compras ESG y Kanban | A | C | – | C | **R** | C | C | I |
| Programa de retorno y valorización | A | C | – | I | C | C | C | **R** |
| Tablero de KPI | C | I | I | **R** | I | I | I | I |
| Revisión PDCA y políticas | **R/A** | C | C | C | C | C | C | C |

### 4.8 Distribución de tareas del equipo (3.1.4)

Escriban los nombres de los integrantes (grupo de 2 a 4). Cada integrante "representa" a un grupo de departamentos y presenta sus metas y KPI.

| Integrante | Departamentos que presenta | Tareas en el informe | Tareas en la presentación (20 min) |
|---|---|---|---|
| Integrante 1: ____________ | Gerencia / Comité de Sustentabilidad + Adm. y Finanzas | Introducción, objetivos, lineamientos (4.1), políticas (5) | Apertura, lineamientos y políticas (5 min) |
| Integrante 2: ____________ | Abastecimiento + Proveedores + Ventas + Diseño | Matriz de riesgo (4.3), metas y KPI de abastecimiento y cliente | Riesgos y eslabón de entrada (5 min) |
| Integrante 3: ____________ | Producción + Bodega y Logística | Plan de acción (4.4), metas y KPI de producción y bodega, BPMN TO-BE | Eslabones de producción y logística (5 min) |
| Integrante 4: ____________ | Logística Inversa + Tablero de KPI | Metas de fin de vida, RACI (4.7), discusión y conclusión | Economía circular, KPI y cierre (5 min) |

**Mecanismo de ajuste:** en cada reunión de avance el grupo revisa el estado de las tareas (semáforo verde/amarillo/rojo). Si una tarea está atrasada o una meta no queda bien fundamentada, se reasigna apoyo desde el integrante con menor carga. Es la misma lógica de la compuerta "¿Metas cumplidas?" del BPMN TO-BE.

---

## 5. Políticas de sustentabilidad asociadas a la mejora continua (3.1.5)

| Política | Declaración | Riesgos que aborda | Dueño |
|---|---|---|---|
| **P1. Cero desperdicio en procesos** | Buzines identifica y elimina mudas en todos sus procesos con 5S, Kanban y Jidoka, y revisa su avance mensualmente en el Comité de Sustentabilidad. | M3, M6, M8, M9, M10 | Coordinador de sustentabilidad |
| **P2. Compras responsables** | Toda compra de tela e insumos sobre el monto definido por Gerencia se hace a proveedores evaluados con criterios ambientales, laborales y de trazabilidad. Se prioriza material reciclado u orgánico y embalaje retornable. | M6, R-S2 | Comprador |
| **P3. Logística baja en emisiones** | Los traslados internos y despachos se planifican de forma consolidada, con rutas optimizadas y medición de su huella de carbono. | M4, M7 | Jefe de bodega / Jefe de producción |
| **P4. Economía circular textil** | Ningún retazo, merma o prenda devuelta se dispone en relleno sanitario sin antes evaluar su reutilización, reciclaje o valorización con un gestor autorizado. | R-S1 | Encargado de economía circular |
| **P5. Dato único y decisiones con evidencia** | Cada dato del pedido se registra una sola vez en el sistema ERP-WMS. Las decisiones de mejora se toman con base en el tablero de KPI. | M5, M12 | Encargado ERP-WMS / Analista KPI |
| **P6. Calidad en la fuente** | Cada operario es responsable de la calidad de su trabajo y está facultado para detener la línea ante un defecto (Jidoka). | M9, M10, M2 | Jefe de producción |

**Revisión de las políticas:** el Comité las revisa una vez al año o cuando un KPI se desvía más de 2 meses seguidos. Se sigue el ciclo PDCA: Planificar (matriz de riesgo), Hacer (plan de acción), Verificar (KPI) y Actuar (ajuste de la política).

---

## 6. Discusión y conclusión

El diagnóstico mostró que las pérdidas más grandes de Buzines (M4, M9, M3) no tienen un responsable único: cruzan Bodega, Producción y Administración. El plan resuelve esto con **agentes dueños de cada meta y cada KPI**. También crea tres departamentos que hoy no existen:

- **Abastecimiento y Compras Sustentables:** cubre el inicio de la cadena (proveedores, Kanban).
- **Logística Inversa y Gestión de Residuos:** cierra el ciclo del textil (economía circular).
- **Comité de Sustentabilidad:** gobierna el plan con PDCA y garantiza la mejora continua.

Si se capturan las mejoras con un escenario conservador del 70 %, el ahorro estimado es de **$16,8–26,6 M/año**. A eso se suman la reducción de emisiones del transporte interno y la valorización de residuos textiles. El modelo `plan_desarrollo_sustentable_TOBE.bpmn` puede abrirse en Bizagi Modeler para presentar el flujo con sus departamentos y agentes.

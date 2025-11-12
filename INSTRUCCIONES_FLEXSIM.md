# Instrucciones para Crear Modelo FlexSim - Bodega Textiles

## Problema Identificado

Los errores que estás experimentando indican problemas de compatibilidad con la estructura interna de FlexSim. Esto puede deberse a:

1. **Versión de FlexSim diferente** - El script fue diseñado para versiones recientes
2. **Comandos obsoletos** - Algunos comandos pueden tener sintaxis diferente
3. **Modelo no inicializado correctamente** - FlexSim esperaba una estructura base

---

## OPCIÓN 1: Usar Script Simplificado (RECOMENDADO)

### Pasos:

1. **Abrir FlexSim**
2. **Crear Nuevo Modelo:** `File > New Model`
3. **Abrir Script Editor:** Presionar `Ctrl + E` (o `Tools > Script Console`)
4. **Copiar el contenido de:** `Bodega_Textiles_FlexSim_Simplified.fsc`
5. **Pegar en el editor**
6. **Ejecutar:** Presionar botón verde "Run" o `F5`

Este script simplificado:
- ✓ No usa comandos avanzados que puedan causar conflictos
- ✓ Crea objetos uno por uno de forma explícita
- ✓ Usa comandos básicos compatibles con más versiones
- ✓ No intenta modificar configuraciones del sistema

---

## OPCIÓN 2: Creación Manual Guiada

Si el script sigue dando problemas, crear el modelo manualmente:

### A. Crear Racks

1. Ir a librería de objetos (lado izquierdo)
2. Arrastrar objeto `Rack` al modelo
3. Hacer clic derecho > Properties
4. Configurar:

**Racks Tipo A (6 metros) - 4 unidades:**
- Nombre: `Rack_6m_01`, `Rack_6m_02`, etc.
- Size: X=6.0, Y=1.2, Z=4.0
- Location: Ver tabla de posiciones abajo

**Racks Tipo B (3 metros - Hombre) - 4 unidades:**
- Nombre: `Rack_3m_Hombre_01`, etc.
- Size: X=3.0, Y=1.2, Z=3.5

**Racks Tipo B (3 metros - Mujer) - 4 unidades:**
- Nombre: `Rack_3m_Mujer_01`, etc.
- Size: X=3.0, Y=1.2, Z=3.5

**Racks Tipo C (2 metros - Picking) - 4 unidades:**
- Nombre: `Rack_2m_Picking_01`, etc.
- Size: X=2.0, Y=1.0, Z=2.5

### B. Crear Zonas (Queue)

1. Arrastrar objeto `Queue` al modelo
2. Configurar propiedades:

- **Area_Recepcion:** Size 4.0 x 3.0, Location (3, 2, 0)
- **Area_Packing_Principal:** Size 4.0 x 3.0, Location (8, 3, 0)
- **Area_Packing_Alternativa:** Size 3.0 x 2.5, Location (15, 4, 0)
- **Area_Merma:** Size 2.0 x 1.5, Location (22, 12, 0)

### C. Crear Equipamiento (Operator)

1. Arrastrar objeto `Operator` al modelo (3 unidades)
2. Nombrar:
   - `Stacker_01` - Apiladora eléctrica
   - `Transpaleta_01` - Transpaleta manual 1
   - `Transpaleta_02` - Transpaleta manual 2

### D. Crear Flujos

1. **Source** (2 unidades):
   - `Source_Recepcion` - para recepción de mercadería
   - `Source_Pedidos` - para generación de pedidos

2. **Processor** (2 unidades):
   - `Processor_Verificacion` - verificación de mercadería
   - `Processor_Packing` - empaquetado

3. **Sink** (1 unidad):
   - `Sink_Salida` - salida de pedidos

### E. Conectar Objetos

1. Mantener presionado `A` en el teclado
2. Hacer clic en objeto origen
3. Hacer clic en objeto destino
4. Soltar `A`

**Conexiones principales:**
- Source_Recepcion → Area_Recepcion → Processor_Verificacion → Racks
- Source_Pedidos → Area_Packing_Principal → Processor_Packing → Sink_Salida

---

## OPCIÓN 3: Verificar Versión de FlexSim

### ¿Qué versión tienes?

1. Abrir FlexSim
2. `Help > About FlexSim`
3. Anotar el número de versión

**Versiones recomendadas:**
- FlexSim 2022 o superior
- FlexSim HC 5.0 o superior

Si tienes una versión anterior a 2020, algunos comandos pueden no ser compatibles.

---

## Tabla de Posiciones de Racks

| Objeto | X | Y | Z |
|--------|---|---|---|
| Rack_6m_01 | 5 | 12 | 0 |
| Rack_6m_02 | 12 | 12 | 0 |
| Rack_6m_03 | 5 | 10 | 0 |
| Rack_6m_04 | 12 | 10 | 0 |
| Rack_3m_Hombre_01 | 3 | 4 | 0 |
| Rack_3m_Hombre_02 | 7 | 4 | 0 |
| Rack_3m_Hombre_03 | 11 | 4 | 0 |
| Rack_3m_Hombre_04 | 15 | 4 | 0 |
| Rack_3m_Mujer_01 | 19 | 4 | 0 |
| Rack_3m_Mujer_02 | 20.5 | 4 | 0 |
| Rack_3m_Mujer_03 | 22 | 4 | 0 |
| Rack_3m_Mujer_04 | 23.5 | 4 | 0 |
| Rack_2m_Picking_01 | 10 | 7 | 0 |
| Rack_2m_Picking_02 | 12.5 | 9 | 0 |
| Rack_2m_Picking_03 | 15 | 7 | 0 |
| Rack_2m_Picking_04 | 17.5 | 9 | 0 |

---

## Parámetros de Simulación Recomendados

### Tiempos de Proceso:
- **Verificación:** Triangular(900, 1050, 1200) segundos (15-20 min)
- **Packing:** Triangular(1800, 2250, 2700) segundos (30-45 min)

### Intervalos de Llegada:
- **Recepción:** Exponential(1800) segundos (30 min promedio)
- **Pedidos:** Exponential(2700) segundos (45 min promedio)

### Velocidades de Equipamiento:
- **Stacker vacío:** 1.2 m/s
- **Stacker cargado:** 0.8 m/s
- **Transpaleta vacía:** 1.0 m/s
- **Transpaleta cargada:** 0.6 m/s

---

## Solución de Problemas

### Si el script simplificado aún falla:

1. **Verificar permisos de usuario** en FlexSim
2. **Reiniciar FlexSim** completamente
3. **Crear modelo manualmente** (Opción 2)
4. **Actualizar FlexSim** a versión más reciente
5. **Contactar soporte de FlexSim** con los mensajes de error específicos

### Errores comunes:

- **"Method find() called on node that does not exist"** → Usar script simplificado
- **"Property value accessed on invalid node"** → El modelo no se inicializó correctamente
- **Problemas con RunPanel/Time Block** → Errores de interfaz, reiniciar FlexSim

---

## Contacto y Recursos

- **FlexSim Documentation:** https://docs.flexsim.com
- **FlexSim Community:** https://answers.flexsim.com
- **Video Tutorials:** https://www.flexsim.com/learning

---

**Fecha:** 12 de Noviembre de 2025
**Versión del documento:** 1.0

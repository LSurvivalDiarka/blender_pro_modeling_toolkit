# Blender Pro Modeling Toolkit

Addon profesional para Blender enfocado en modelado, hard surface, materiales, UVs, limpieza de escenas y preparación de assets para videojuegos.

> Made by **Diarka Studio**  
> Created by **Saúl**  
> Versión detectada en `blender_manifest.toml`: **0.1.6**

---

> Capturas de la interfaz próximamente.

## Descripción general

**Blender Pro Modeling Toolkit** nace como una herramienta práctica para acelerar mi trabajo dentro de Blender y tener en un solo panel muchas utilidades que uso al crear assets, limpiar escenas, preparar materiales y trabajar con una base más ordenada.

Está pensado para modelar más rápido, organizar mejor los archivos, crear formas base, trabajar hard surface, revisar UVs, preparar materiales, hacer baking y dejar assets más limpios antes de llevarlos a un flujo de videojuegos o producción 3D.

El addon se integra en el **Viewport 3D**, dentro del panel lateral de Blender, en la pestaña **Pro Toolkit**.

## Funciones principales

| Suite | Enfoque |
|---|---|
| **Quick Modeling Tools** | Selección, vértices, aristas, caras, pivotes, modificadores rápidos y limpieza básica. |
| **Pro Modeling Creation** | Creación de blockouts, arquitectura modular, props, productos, formas base, escalas y helpers. |
| **Profile Revolve / Lathe Pro** | Perfiles laterales, trazado sobre referencia y revolución con Screw para piezas cilíndricas. |
| **Hard Surface Pro** | Cutters, booleanos, bevels, weighted normals, paneles técnicos, rejillas y auditoría hard surface. |
| **Pro UV Suite** | Gestión de UV maps, seams, unwrap, islas, texel density, checkers y auditoría UV. |
| **Pro Cel Shading Suite** | Presets toon/cel, outlines, conversión de materiales y helpers de iluminación. |
| **Character / Organic / Retopo Pro** | Limpieza orgánica, soporte para modelos generados por IA, simetría, retopo y preparación game ready. |
| **Material / Texture / Baking Pro** | Auditoría de materiales, texturas, PBR, materiales procedurales, baking y preparación para Unity/game assets. |

### Quick Modeling Tools

Incluye herramientas rápidas para tareas comunes de modelado: selección de n-gons, tris, non-manifold, bordes abiertos, seams, crecimiento/reducción de selección, relax, flatten, merge por distancia, extrude, inset, solidify, circularize y operaciones de pivote/origen.

También incorpora accesos rápidos a modificadores como **Mirror**, **Solidify**, **Bevel** y **Weighted Normal**, además de una limpieza básica y auditoría del objeto activo.

### Pro Modeling Creation

Suite para crear bases de modelado con medidas útiles y nombres organizados. Incluye:

- módulos de pared, suelo, habitaciones, puertas, ventanas, pilares, vigas, escaleras, mostradores y estanterías;
- bases de productos y props como cajas, latas, botellas, bolsas, bricks, etiquetas, carteles, cajas registradoras, neveras y carros;
- formas auxiliares como rounded boxes, pipes, cables, handles, rails, vents, panels, frames, slots, arcos y cutters simples;
- herramientas de origen, escala, snap, medición y referencias de tamaño humano;
- presets específicos de **Supermarket Flower** para blockout y organización.

### Profile Revolve / Lathe Pro

Sistema para crear objetos por revolución a partir de perfiles laterales editables. Está pensado para formas como botellas, latas, tarros, tapas, pomos, columnas, jarrones o envases.

La suite incluye creación de perfiles en curva o malla, eje de referencia, centrado de imagen de referencia, modos de trazado, Screw/Revolve 360, cierre de tapas, bevel, weighted normals y conversión segura a malla cuando haga falta.

El modo **Draw / Trace** prepara Blender para dibujar o calcar una media silueta sobre una imagen lateral. No convierte una imagen automáticamente en 3D; deja la escena lista para trazar el perfil y luego aplicar la revolución.

### Hard Surface Pro

Herramientas para un flujo hard surface más directo:

- creación de cutters de caja, cilindro, slot, panel y agujeros;
- booleanos Difference, Union e Intersect con flujo no destructivo cuando procede;
- aplicación segura de booleanos con backup;
- creación de paneles, grooves, slots, rejillas, vents y detalles mecánicos;
- bevels inteligentes y weighted normals;
- alineación, duplicado, rotación, mirror y organización de cutters;
- auditoría para detectar escala sin aplicar, n-gons, non-manifold y problemas típicos del flujo hard surface.

También incluye detalles mecánicos y presets legacy/opcionales relacionados con Supermarket Flower.

### Pro UV Suite

Conjunto de utilidades para preparar y revisar UVs:

- creación, duplicado, renombrado, activación y borrado de UV maps;
- marcado y limpieza de seams;
- auto seams para hard surface u orgánico;
- presets de unwrap para props, arquitectura, personajes, lightmaps y otros casos;
- pack, average scale, minimize stretch, rotación, flip, fit 0-1 y alineación de islas;
- cálculo y ajuste de texel density;
- materiales checker para revisar distorsión;
- auditoría UV con selección de overlaps, UVs fuera de 0-1, flipped UVs y zero-area.

Algunas comprobaciones UV, como ciertos solapamientos, se tratan como estimaciones cuando el propio addon lo indica.

### Pro Cel Shading Suite

Suite para aplicar looks toon/cel sin perder de vista los materiales originales. Incluye presets, controles de color, sombras, rim light, outlines, conversión de materiales y luces de apoyo.

El flujo de **Texture Preserving Toon** está pensado para duplicar o proteger materiales originales cuando se convierte un objeto a toon, manteniendo texturas base cuando el material las permite.

La parte de **Line Art** aparece marcada como experimental dentro del panel, porque depende del comportamiento de Grease Pencil y Blender puede variar según versión.

### Character / Organic / Retopo Pro

Herramientas de apoyo para personajes, criaturas, mallas orgánicas y retopología:

- limpieza orgánica, relax, inflate/deflate, smooth by surface y merge seguro;
- auditoría de modelos generados por IA, detección de zonas densas, piezas sueltas, normales malas y riesgos de atlas;
- preparación de una malla fuente para retopo;
- herramientas de simetría, mirror seguro y plano de simetría;
- creación de setup de retopo con Shrinkwrap/Mirror, planos, strips y patches;
- helpers para quad patches, edge strips, bridge, fill, project, relax y snap a superficie;
- auditoría de topología, edge flow y retopo readiness;
- guías de escala humana, marcadores y preparación para sculpt;
- duplicado de exportación y placeholders de LOD para preparación game ready.

### Material / Texture / Baking Pro

Suite para revisar y preparar materiales y texturas antes de exportar o bakear:

- auditoría de materiales con detección de slots vacíos, duplicados, materiales sin uso, texturas perdidas, rutas absolutas y problemas PBR;
- limpieza de materiales, backups, renombrado y asignación de IDs/debug;
- búsqueda, relink, empaquetado, rutas relativas/absolutas y reporte de texturas;
- creación de materiales PBR desde valores o carpetas de texturas;
- presets de materiales procedurales;
- revisión de atlas y UVs para texturas;
- colecciones de baking High/Low/Cage/Output;
- creación de imágenes de bake y asignación de nodos;
- bake de Normal, AO, Diffuse, Roughness, Emission, Color ID y Combined;
- flujo High to Low con pairing por nombre o selección;
- auditoría de preparación para Unity/materiales de juego.

La suite prepara y valida materiales para un flujo de juego, pero no se presenta como un exportador completo a Unity.

## Instalación

1. Descarga el ZIP del addon.
2. Abre Blender 4.2 o superior.
3. Ve a `Edit > Preferences > Add-ons`.
4. Pulsa `Install from Disk...`.
5. Selecciona el ZIP del addon.
6. Activa **Blender Pro Modeling Toolkit**.
7. En el Viewport 3D, pulsa `N`.
8. Abre la pestaña **Pro Toolkit**.

El addon aparece en el panel lateral del **Viewport 3D**.

## Uso básico

1. Abre Blender.
2. Pulsa `N` en el Viewport 3D.
3. Entra en la pestaña **Pro Toolkit**.
4. Elige la suite que necesites.
5. Usa las herramientas por bloques según el tipo de tarea.

Ejemplos de uso:

- crear un perfil lateral de botella y aplicar **Lathe / Revolve 360**;
- crear un cutter y añadir un booleano Difference a una pieza hard surface;
- revisar UVs con checker, texel density y auditoría;
- convertir materiales a un look toon preservando texturas cuando sea posible;
- crear un material PBR desde una carpeta de mapas;
- preparar un setup High/Low para baking;
- limpiar materiales, revisar texturas perdidas y generar reportes;
- auditar un modelo orgánico o generado por IA antes de retopología.

## Estado del proyecto

Esta versión está pensada como una versión funcional para uso personal/profesional y publicación inicial en GitHub.

El addon reúne muchas herramientas reales de producción y varias suites amplias dentro del panel **Pro Toolkit**. Aun así, algunas partes pueden seguir evolucionando en futuras versiones, especialmente los flujos más sensibles a cambios de Blender, como Line Art/Grease Pencil, validaciones avanzadas y mejoras de exportación.

## Para qué lo estoy usando

Este addon nace como parte de mi flujo de trabajo para crear escenarios, props y assets para proyectos 3D en Blender.

La idea es poder bloquear formas rápido, modelar piezas hard surface, preparar materiales, revisar UVs, limpiar escenas y dejar los assets más listos para pipelines de videojuegos sin saltar constantemente entre herramientas sueltas.

## Roadmap

- Mejorar la interfaz visual y la lectura de paneles.
- Añadir más flujos guiados paso a paso.
- Refinar herramientas hard surface y boolean workflow.
- Mejorar validaciones para assets de videojuegos.
- Ampliar ejemplos de uso y documentación.
- Añadir capturas reales de la interfaz.

## Créditos

Made by Diarka Studio  
Created by Saúl



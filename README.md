<div align="center">

<br/>

```
██████╗  ██████╗ ██████╗  ██████╗  ██████╗ ██╗   ██╗██╗██████╗ ███████╗
██╔══██╗██╔═══██╗██╔══██╗██╔═══██╗██╔════╝ ██║   ██║██║██╔══██╗██╔════╝
██████╔╝██║   ██║██████╔╝██║   ██║██║  ███╗██║   ██║██║██║  ██║█████╗  
██╔══██╗██║   ██║██╔══██╗██║   ██║██║   ██║██║   ██║██║██║  ██║██╔══╝  
██║  ██║╚██████╔╝██████╔╝╚██████╔╝╚██████╔╝╚██████╔╝██║██████╔╝███████╗
╚═╝  ╚═╝ ╚═════╝ ╚═════╝  ╚═════╝  ╚═════╝  ╚═════╝ ╚═╝╚═════╝ ╚══════╝
```

### _Simulaciones industriales con FANUC: pick & place, soldadura y modificación de útiles_

<br/>

[![Roboguide](https://img.shields.io/badge/Software-ROBOGUIDE-FFD700?style=for-the-badge)](https://www.fanuc.eu/es/es/robots/accesorios-robots/roboguide)
[![FANUC](https://img.shields.io/badge/Robot-FANUC-FFD700?style=for-the-badge&logoColor=black)](https://www.fanuc.eu/)
[![Soldadura](https://img.shields.io/badge/Proceso-Soldadura_y_Pick%26Place-1a1a2e?style=for-the-badge)]()
[![Prácticas](https://img.shields.io/badge/Contexto-Prácticas_Curriculares-0077B6?style=for-the-badge)]()

<br/>

> **Prácticas Curriculares** · Sector de Automatización Industrial · Ingeniería Robótica · 2025

</div>

---

## 🏭 ¿Qué contiene este repositorio?

Simulaciones industriales desarrolladas con **FANUC ROBOGUIDE** durante las prácticas curriculares del Grado en Ingeniería Robótica, en una empresa del sector de la automatización industrial.

Los proyectos abarcan dos tipos de procesos industriales — **pick & place** y **soldadura robotizada** — con robots FANUC en configuraciones reales de producción, incluyendo tracks, peanas y volteadores personalizados.

> ⚠️ Los archivos de simulación pertenecen a la empresa. Este repositorio recoge únicamente las descripciones técnicas de los proyectos realizados.

---

## 🔬 Simulaciones Realizadas

### 1 — Pick & Place para Línea de Galvanizado

Automatización de la carga de una plataforma de galvanizado mediante un robot montado sobre un **track central**, con movimientos de precisión en múltiples niveles.

| Elemento | Detalle |
|----------|---------|
| Software | FANUC ROBOGUIDE |
| Robot | R2000IC/270F sobre track lineal |
| Herramienta | Ventosa de succión |
| Proceso | Pick & place de piezas y soportes |

**Descripción del ciclo:**
1. El robot se desplaza al extremo derecho del track y recoge dos soportes
2. Los coloca en el nivel más bajo de la plataforma central
3. Se traslada al extremo opuesto y recoge la pieza a galvanizar
4. Posiciona la pieza sobre los soportes instalados
5. El ciclo se repite completando los 5 niveles de la estructura

<div align="center">

[![Pick & Place Galvanizado](https://img.youtube.com/vi/6peAJw9FVZM/maxresdefault.jpg)](https://www.youtube.com/watch?v=6peAJw9FVZM)

</div>

---

### 2 — Soldadura de Chasis de Columna Estructural

Soldadura de una **pieza de grandes dimensiones** tanto en su cara exterior como interior, con control de colisiones y singularidades en el espacio de trabajo interior.

| Elemento | Detalle |
|----------|---------|
| Software | FANUC ROBOGUIDE |
| Robot | ARC MATE 120 sobre peana elevadora + track personalizado |
| Periférico | 2 volteadores personalizados |
| Reto principal | Evitar colisiones y singularidades en el interior de la pieza |

<div align="center">

[![Soldadura Columna 1](https://img.youtube.com/vi/OQWF42v-As4/maxresdefault.jpg)](https://www.youtube.com/watch?v=OQWF42v-As4)


</div>

---

### 3 — Modificación de Útil: Antorcha con Sensor de Detección

Variante del proyecto anterior en la que el cliente solicitó incorporar una **cámara con láser** en la antorcha para detectar automáticamente la ranura de soldadura.

**Problema:** el reducido espacio de trabajo en el interior de la pieza hacía inviable la antorcha modificada en ciertas zonas.

**Solución propuesta:** técnica de **Touch Sensing** — detección de la posición exacta de la junta usando la propia antorcha como sensor, realizando un contacto sin arco antes de iniciar el cordón. Se comunicó al cliente qué porcentaje del proceso era realizable con este método.

> Este proyecto ilustra el flujo real de trabajo con un cliente: análisis de viabilidad, identificación de limitaciones y propuesta de alternativa técnica.

<div align="center">
[![Soldadura Columna 2](https://img.youtube.com/vi/adYUza0G9CU/maxresdefault.jpg)](https://www.youtube.com/watch?v=adYUza0G9CU)
</div>
---

### 4 — Soldadura de Escalera Metálica

Soldadura de **26 barrotes** en los laterales de una escalera metálica, con una estrategia de trayectorias optimizada para minimizar el tiempo de ciclo.

| Elemento | Detalle |
|----------|---------|
| Software | FANUC ROBOGUIDE |
| Robot | ARC MATE 120 sobre peana elevadora + track personalizado |
| Periférico | 2 volteadores personalizados |
| Cordones | 3 por extremo en primer/último barrote · 1 lateral + 1 superior en el resto |

**Estrategia de optimización:** se completó primero el lateral derecho íntegro y después el izquierdo, evitando desplazamientos alternados innecesarios y reduciendo los tiempos muertos del robot.

<div align="center">

[![Soldadura Escalera](https://img.youtube.com/vi/HjnFqnhfdsM/maxresdefault.jpg)](https://www.youtube.com/watch?v=HjnFqnhfdsM)

</div>

---

## 🛠️ Tecnologías

- **FANUC ROBOGUIDE** — programación offline y simulación
- **TP (Teach Pendant programming)** — lenguaje de programación FANUC
- Tracks lineales y peanas para ampliar el espacio de trabajo
- Volteadores personalizados para acceso a geometrías complejas
- Touch Sensing para detección automática de juntas de soldadura

---

## 📚 Contexto

**Tipo:** Prácticas Curriculares · Grado en Ingeniería Robótica  
**Sector:** Automatización industrial · Soldadura robotizada  
**Autor:** Nicolás Fernández Blánquez  
**Año:** 2025

---

<div align="center">

_Simulaciones desarrolladas sobre requerimientos reales de clientes industriales._

</div>

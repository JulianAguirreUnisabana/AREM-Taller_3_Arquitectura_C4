# 🗒️ Registro de Trabajo en Clase - Taller 3: Arquitectura Actual del Sistema con el Modelo C4

## 📆 Fecha de la sesión
6 de septiembre de 2026

## 👥 Integrantes presentes
- Brayan Presiga
- Julián Aguirre
- Jorge Alarcon

---

# Nivel C1 – Vista de Contexto

## 🧠 Actividades realizadas en clase
- **¿Qué se discutió con el equipo?** Se analizó el caso base de RedExpress, una empresa nacional de logística y envíos, con el fin de identificar los actores principales, los sistemas que componen su arquitectura y las relaciones entre ellos.
- **¿Qué decisiones de modelado se tomaron?** Se definió representar el nivel C1 (Vista de Contexto) mostrando tres actores (Usuario Final, Mensajero y Operador Logístico) interactuando con la Plataforma RedExpress como sistema central, y dos sistemas externos (API de Notificaciones y Proveedor de Geolocalización) integrados mediante APIs REST.
- **¿Qué herramientas se usaron?** Draw.io, para construir el diagrama de contexto de forma digital.
- **¿Qué parte del trabajo se alcanzó a desarrollar?** Se completó el diagrama C1 con sus actores, sistemas y relaciones, junto con la descripción de cada elemento.
  
## 🧩 Boceto inicial del modelo
> Diagrama de contexto (C1) elaborado en draw.io, mostrando los actores (Usuario Final, Mensajero, Operador Logístico), el sistema central (Plataforma RedExpress) y los sistemas externos (API de Notificaciones, Proveedor de Geolocalización).

## 📋 Tabla de actores, entidades o componentes

| Nombre del elemento | Tipo | Descripción | Responsable |
|---------------------|------|-------------|-------------|
| Usuario Final | Actor | Cliente que rastrea envíos y agenda recogidas desde la app/web | Cliente |
| Mensajero | Actor | Realiza entregas y actualiza el estado de los paquetes en tiempo real | Cliente |
| Operador Logístico | Actor | Gestiona rutas y despachos desde el centro de distribución | Cliente |
| Plataforma RedExpress | Sistema (Software System) | Sistema central que integra gestión de paquetes, seguimiento GPS, motor de rutas y alertas | RedExpress |
| API de Notificaciones | Sistema externo (Software System) | Envía alertas de estado por API REST a usuarios y mensajeros | Proveedor externo |
| Proveedor de Geolocalización | Sistema externo (Software System) | Provee coordenadas y cálculo de rutas por API REST | Proveedor externo |

## 🧮 Análisis del modelo C1

**Cómo se estructura el modelo entregado:**
El modelo C1 se estructura alrededor de un sistema central, la Plataforma RedExpress, que concentra la lógica del negocio. Alrededor de este sistema se ubican tres actores humanos (Usuario Final, Mensajero, Operador Logístico), cada uno con una relación funcional distinta hacia la plataforma, y dos sistemas externos que se comunican con ella mediante interfaces API REST. Esta estructura sigue el estándar del modelo C4 para el nivel de contexto: mostrar el sistema de interés en el centro, sin detallar su arquitectura interna, y representar únicamente sus fronteras de interacción con actores y sistemas externos.

**Cómo representa las necesidades del cliente:**
El diagrama refleja las necesidades operativas descritas en el caso de RedExpress: el rastreo en tiempo real de paquetes (relación del Usuario Final), la actualización del estado de entregas en campo (relación del Mensajero), la coordinación de rutas y despachos (relación del Operador Logístico), y la dependencia de servicios externos para notificar a los usuarios y calcular rutas óptimas. De esta forma, el modelo captura tanto la interacción de los usuarios finales como la infraestructura de soporte que la empresa necesita para escalar su operación.

**Qué supuestos se tomaron:**
- Se asumió que la comunicación entre la Plataforma RedExpress y los sistemas externos (Notificaciones y Geolocalización) se realiza exclusivamente mediante API REST, sin considerar otros protocolos.
- Se asumió que el Operador Logístico y el Mensajero interactúan directamente con la misma plataforma central, y no con sistemas separados (como una web para operadores mencionada en el contexto original), dado que el diagrama entregado no los distingue como contenedores separados.
- Se asumió que las bases de datos, balanceadores de carga y demás elementos de infraestructura no se representan en este nivel, ya que corresponden al nivel C2 (Vista de Contenedores).
- Se asumió que "Usuario Final" agrupa tanto a clientes individuales como a clientes corporativos que usan el dashboard de seguimiento, sin diferenciarlos como actores separados en este nivel.

---

# Nivel C2 – Vista de Contenedores

## 🧠 Actividades realizadas en clase
Describa brevemente qué se hizo durante la sesión:
- ¿Qué se discutió con el equipo?
- ¿Qué decisiones de modelado se tomaron?
- ¿Qué herramientas se usaron (papel, pizarra, draw.io, Astah)?
- ¿Qué parte del trabajo se alcanzó a desarrollar?

## 🧩 Boceto inicial del modelo
> Diagrama de contexto (C2) elaborado en draw.io

## 📋 Tabla de actores, entidades o componentes (si aplica)

| Nombre del elemento | Tipo | Descripción | Responsable |
|---------------------|------|-------------|-------------|
| Ej: Paciente        | Actor | Usuario que agenda una cita médica | Cliente |

## 🧮 Análisis del modelo C2
_(Pendiente de completar)_

---

## 🔁 Tareas definidas para complementar el taller
| Tarea asignada | Responsable | Fecha estimada |
|----------------|-------------|----------------|
| Diseño y documentación del Diagrama c1 | Julián Aguirre | 06/09 |
| Diseño y documentación del Diagrama c2 | Jorge Alarcon | 06/09 |
| Creación de los diagramas en draw.io | Brayan Presiga | 06/09 |

---
_Este documento resume el trabajo colaborativo realizado durante la sesión del Taller 3: Arquitectura Actual del Sistema con el Modelo C4 en el curso AREM - Universidad de La Sabana._

# TP4-AM1


Instalación audiovisual interactiva desarrollada en **Processing** para la materia **Artes Multimediales I — Cátedra Pirotta (UNA)**.

## Descripción conceptual

La obra explora la tensión entre el control algorítmico y la resistencia física a partir del concepto de panóptico analizado por Michel Foucault. Al ingresar al espacio de captura, una cámara de circuito cerrado (CCTV) registra al participante en monocromo clínico y lo encasilla dentro de una retícula geométrica de datos biométricos y *bounding boxes*.

> *"Donde hay poder, hay resistencia"*.

Al extender los brazos, abrir las manos y realizar ademanes frente a la proyección, el cuerpo quiebra la norma geométrica del sistema: las manos operan como un disruptor óptico que desgarra, desplaza y licúa en tiempo real la imagen de vigilancia que intenta capturarlo.

## Funcionamiento técnico

* **Visión por computadora (`OpenCV for Processing`):** Sustracción de fondo en tiempo real y detección de contornos (*blob tracking*) para diferenciar la masa corporal estática de las extremidades en movimiento.
* **Deformación de imagen (*Displacement / Warp*):** Manipulación directa de la matriz de píxeles del flujo de video (`processing.video`), generando ondas radiales fluidas alrededor de los puntos de movimiento detectados.
* **Estética CCTV & HUD:** Interfaz superpuesta con telemetría biométrica, miras de seguimiento, líneas de escaneo (*scanlines*) y filtrado tonal de vigilancia.
* **Comunicación OSC (`oscP5`):** Transmisión de coordenadas normalizadas (`/panoptico/posicion`) y área de expansión corporal (`/panoptico/area`) por puerto UDP para vinculación con entornos sonoros externos.

## Requisitos y ejecución

1. **Software:** Processing 4.
2. **Librerías necesarias** (instalar desde *Herramientas > Administrar herramientas > Libraries*):
   * `Video` (Processing Foundation)
   * `OpenCV for Processing` (Greg Borenstein)
   * `oscP5` (Andreas Schlegel)

## Créditos

* **Autoras:** Rocío Sosa y Azul Cejas.
* **Institución:** Universidad Nacional de las Artes (UNA) — Artes Multimediales I (Cátedra Pirotta).

# Entradas-y-Salidas-Análogas

## 1. Digital vs Análogico

|                                               Señales Digitales                                              | Señales Análogicas                                                                                         |
|:------------------------------------------------------------------------------------------------------------:|------------------------------------------------------------------------------------------------------------|
| Son aquellas que solamente pueden tomar 2  valores de tensión para representar un nivel alto y un nivel bajo | Son aquellas que pueden tomar cualquier nivel de tensión dentro  de un rango determinado de funcionamiento |
|             Cualquier nivel intermedio es forzado a uno de estos 2  estados a través de hardware             | La mayoriá de las señales del ambiente son análogicas:  Ej: Temperatura, luz, sonido                       |

## 2. Conversión Digital a Análoga 

### 2.1 Salida Análoga 

- Algunos microcontroladores poseen salidas analógicas que permiten representar valores binarios en una señal eléctrica de voltaje

- Para el caso en que no se tenga salida analógica:
  - Usar señal de PWM y aplicar un filtro en la salida para obtener el valor promedio
  - Usar un circuito resistivo de ponderación binaria

### 2.2 Ponderación con circuito resistivo 

Cada bit de salida se conecta a una Resistencia que por medio de sus valores va ponderando cada bit por 2n 

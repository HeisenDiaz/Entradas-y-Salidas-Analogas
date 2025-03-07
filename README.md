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

## 3. Conversión Análoga a Digital 

- Teniendo en cuenta que el microcontrolador es un dispositivo digital
- Las señales analógicas no podrán ser procesadas directamente por el microcontrolador
- Es necesario realizar una conversión de la señal análogica a una representación digital que pueda ser procesada por el microcontrolador

### 3.1 Procedimiento de conversión 

#### 3.1.1 Muestreo

- Medir valores de voltaje cada cierto tiempo
- Se mide como el número de veces que se mide en 1 segundo por lo tanto la unidad es Hz
- La tasa de muestreo debe ser mínimo del doble de la frecuencia de la señal que se está muestreando

#### 3.1.2 Cuantificación 

- La señal análoga se convierte en una serie de valores que corresponden a cada una de las medidas tomadas en el muestreo

#### 3.1.3 Codificación 

- Se asignan valores de tipo binario a cada uno de los valores de la cuantización
- Los valores a usar los define el diseñador de acuerdo al tipo de información obtenida en la cuantización
- Lo más usual es que se utilice código binario para representar cada valor de voltaje

## 4. Técnicas de conversion ADC

- Flash Converter
  
  | TIPO            | DESVENTAJA                                                                  |
  |-----------------|-----------------------------------------------------------------------------|
  | Flash Converter | Para cada nivel de comparación se require hardware adicional,  son costosos |
       
- Tracking Converter

  | TIPO                | DESVENTAJA                                                                             |
  |---------------------|----------------------------------------------------------------------------------------|
  |  Tracking Converter | Requiere tiempo para engancharse, no responde muy bien ante señales de cambios rapidos |

- Successive Approximation Converter (SAR)  

  | TIPO                                | VENTAJA                                                                         |
  |-------------------------------------|---------------------------------------------------------------------------------|
  | Successive Approximation  Converter | En la mayoría de microcontroladores este es el tipo de conversor que se utiliza |

  ### 4.1 Algunas características

- La mayoria de microcontroladores tiene varios canales de conversion ADC

- En la mayoría de ocasiones solo hay un conversor que multiplexa sus canales de entrada:

  - Modo sencillo
  - Modo continuo

- El inicio de la conversión puede depender de:
  
  - Usuario/código
  - Barrido en entradas
  - Interrupción
  - Timer

## 5. Conclusiones 

- Identificar las diferencias claves entre las señales digitales y análogas
- Analizamos el procedimiento de conversión de señales análogas a digitales
- Aprendimos las idferentes tecnicas de conversión ADC


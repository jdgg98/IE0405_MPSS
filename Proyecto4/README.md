# Proyecto 4

En este proyecto se presenta una introdución a temas fundamentales de 
la ingeniería de comunicaciones, de manera que se realiza la simulación
de un sistema de transmisión de imágenes de baja resolución. Este trabajo
a su vez, se desarrolla con el objetivo de aplicar el conocimiento adquirido
sobre pocesos estocásticos en el análisis de la modulación digital.

## Autor

- Estudiante: Jafet David Gutiérrez Guevara
- Carné: B73558
- Grupo: 1

  
## Documentation

### 4.1 - Modulación 16-QAM

Para la primera parte de este proyecto se realizó la simulación de un 
sistema de comunicaciones, utilizando una modulación 16-QAM. Para
ello se modificaron las funciones modulador y demodulador, vistas en la
sección 3 del apartado teórico, para adaptarlas a la modulación requerida.
Los resultados del sistema simulado se muestran en la siguiente figura:

[![tx-rx.png](https://i.postimg.cc/qRkrn2Nf/tx-rx.png)](https://postimg.cc/v1SCwg7X)

Se puede ver que la imagen recuperada es muy similar a la imagen transmitida, 
aunque también se puede advertir claramente que la recuperada presenta cierto ruido. 
Este es un buen resultado tomando en cuenta que parte de la información de la 
imagen siempre se perderá durante la modulación 16-QAM. Además cabe mencionar que
la simulación se realizó con 4063 errores, para un BER de 0.0096.

Por otro lado, a continuación se presentan las ondas a través del tiempo de la señal 
modulada por 16-QAM, la señal modulada al dejar el canal y la señal demodulada, respectivamente:

[![se-ales.png](https://i.postimg.cc/G2fNXDXS/se-ales.png)](https://postimg.cc/vgW3B4FW)

### 4.2 - Estacionaridad y ergodicidad

En esta sección se realizaron pruebas de estacionaridad y ergodicidad a la señal modulada `senal_Tx`.
Los resultados de dichas pruebas se presentan en las siguientes dos gráficas:

[![ergod.png](https://i.postimg.cc/9fFnVbSn/ergod.png)](https://postimg.cc/BjkgBTJT)

[![corr-teo.png](https://i.postimg.cc/vTTpts5M/corr-teo.png)](https://postimg.cc/dZMHJgWS)

En los resultados se puede observar que la señal promedio tiene una oscilación amortiguada
alrededor de la línea del valor teórico. Por lo tanto, aunque el promedio estadístico no
coincide completamente, se puede afirmar que sí existe cierta ergodicidad. Por otra parte,
también se puede concluir que las ondas en las dos gráficas son estacionarias, debido a que
ambas conservan el mismo comportamiento a través del tiempo.

### 4.3 - Densidad espectral de potencia

Para esta última parte del proyecto se determinó y gráfico la densidad espectral de potencia 
para la señal modulada `senal_Tx`. En la siguiente figura se muestran los resultados obtenidos:

[![densidad.png](https://i.postimg.cc/vH6KYXzP/densidad.png)](https://postimg.cc/0bPnZYhm)

Al analizar la gráfica construida se puede concluir que el componente más importante es el de 
5000 Hz, mientras que los picos que se encuentran a su alrededor son los componentes de frecuencia
de la onda moduladora. Este resultado tiene sentido, considerando que para la simulación la frecuencia 
de la portadora se definió precisamente en 5000 Hz.

### Universidad de Costa Rica 

#### Facultad de Ingeniería

#### Escuela de Ingeniería Eléctrica

# Kampfi - 2022
Inspirado por los errores tecnicos y la mala suerte, Kampfi fue creado para maximizar la cantidad de cosas que podrian salir mal al hacer girar un pedazo de acero a la velocidad del ventilador en el radiador de un sedan. El equivalente battlebotiano de lo que sucede cuando le das un ak-47 a un mono.

![Kampfi](/multimedia/KampfiFinal.jpeg)

## Integrantes
- Antonia Gutierrez - FCFM
- Benjamín Gonzalez - FCFM
- Joaquin Camhi - FCFM
- Matías Carvajal - FCFM

## Descripción del proyecto
Kampfi es un battlebot blindado con aluminio compuesto y acero. Como arma tiene instalada una hélice de acero en la parte delantera, la cual gira mediante un motor de 12 volts a una velocidad suficiente para romper el robot contrincante. Tiene un tren de traccion compuesto por 2 ruedas delanteras energetizadas por motores de 12 volts, y una rueda trasera no actuada. 

### Forma del robot
La forma triangular de Kampfi asegura que sea difícil de ser destruído por algun ataque superior (como ejemplo, un bot que ataca mediante un martillo), además le da la capacidad de ser facil de armar y desarmar en caso de que sean necesaria reparaciones, dado a que se compone unicamente de panales cuadrados y triangulares, y la base se encuentra conectada a la coraza mediante tornillos fáciles de remover.

### Estrategia utilizada
#### Ofensiva
Kampfi esta equipado de una hélice delantera angulada en 45° con respecto al horizonte. Para atacar se acerca a su victima y al activar el giro de la hélice es capas de destruír cualquier pieza impresa en filamento plastico, separar uniones entre paneles que componen la armadura, doblar corazas metalicas y penetrar pedazos de aluminio compuesto debido al perfil con puntas en las esquinas del arma. Para atacar se debe activar el arma para que empieze a girar y se debe conducir hacia el contrincante en un angulo, idealmente golpeando por el lado izquierdo para aprovechar que la helice gira en sentido antihorario e intentar levantar y desestabilizar al contrintante. 

#### Defensiva
Debido al lento movimiento del robot no es práctico intentar evitar ataques enemigos, la principal defensa es la ofensa: Resistir a los golpes enemigos mediante la coraza de aluminio compuesto y acero, e intentar aterrizar un golpe certero al mecanismo de transmision del arma del contrincante, idealmente desarmandolo. De forma experimental se ha determinado que la armadura es capaz de resistir ataques de armas tipo "spinner", cilindros o discos con perfiles girando a altas velocidades.

#### Uso del arma
La arma se puede activar o desactivar remotamente, se recomienda activar el arma previo al ataque para que gire a una velocidad suficiente como para hacer daño, y desactivar el arma una vez alcanzada una rotación suficiente para evitar gastar la batería principal del robot, dejando que la inercia rotacional del rectangulo de acero le proporcione el daño al enemigo. Si se activa el arma y debido a alguna resistencia (la helice esta atrapada en el cuerpo del contrincante, o en la malla del ring) no gira la helice se debe desactivar inmediatamente el arma, para evitar sobrecalentar los electronicos del robot, junto con el gasto de bateria asociado, el motor usado tiene una gran velocidad de rotacion pero bajo torque: Si no empieza a girar la hélice una vez activada el arma, lo mas probable es que nunca empieze a girar debido a que la resistencia es mayor al torque del motor.

#### Distribución de armadura
Las defensas del robot estan distribuidas de forma relativamente equitativa: El frente esta protegido por el motor de la helice y la helice en sí, los lados tienen aluminio compuesto, y debido a que hay una distancia de un par de centimetros de las laminas de este material y los componentes internos es difícil que se vean dañados por ataques laterales, la parte superior del robot es especialmente resistente a ataques de martillos como se explicó en la seccion "Forma del robot", y la parte trasera es protegida por dos barras paralelas de acero. Debido al peso del robot y a la forma de este, los ataques con objetivo de voltear al enemigo son ineficaces en Kampfi.

### Movimiento
El movimiento y la operación del robot se logran mediante una simple aplicación movil. 6 botones, 4 organizados en una cruz y 2 paralelos, abajo de esta, permiten el movimiento y uso del arma, respectivamente. Los botones de movimiento realizan la accion deseada mientras se presiona el botón (si se desea ir hacia adelante, se presiona el boton correspondiente y se suelta una vez llegado al punto deseado), y el arma opera mediante un toggle on/off: Un boton activa la rotación y otro la detiene. Se tomó la desición de no hacer que el mismo botón prenda y apague el arma por razónes de seguridad, para asegurar que siempre se puede apagar el arma con un boton, y así estar seguro que efectivamente se apagó el arma (ya que esta suele seguir girando una vez apagada debido a la inercia rotacional explicada previamente).

## Diagrama funcional
![Diag. Inicio Bot](/multimedia/flowchart%20inicio.png)

![Diag. Movimiento Bot](/multimedia/flowchart%20movimiento.png)

![Diag. Ataque Bot](/multimedia/flowchart%20ataque.png)

## Paso a Paso
### Materiales

- Plancha de aluminio compuesto
- Plancha de acero inoxidable cortada en rectangulos x3
- Puente H de 12V
- Relay 5Vdc de 1 canal
- Arduino Uno
- Regulador de voltaje 7 V a 5 V
- Motor de radiador (12V), u análogo.
- Filamento plastico PLA
- Bateria 11.1 V 1500mAide (o idealmente de alto mA por hora) 
- Bateria 7.4 V 1200 mA
- Cables
- Tornillos
- Tuercas
- Madera
- Pintura en Aerosol plateada y roja
- 2 motores de rueda 12 V + cajas de transferencia 
- 2 ruedas de goma


### Herramientas

- Taladro
- Router CNC
- Impresora 3D
- Llave inglesa
- Destornillador phillips
- Sierra Circular para madera
- Martillo
- Cautin, y estaño


### Procedimiento

1) Descargar todos los archivos ".f3z" de las piezas, el codigo ".ino" de arduino y el ".apk" de la app
2) Realizar el circuito del bot de acuerdo a los diagrama
3) Cortar las piezas de la base y la coraza en el Router CNC a través del archivo "piezas coraza.f3z" y "base.f3z"
4) Cortar piezas de madera (en archivo "ensamblado.f3z") que permiten las uniones del ensamble. Utilice su herramienta de mayor comodidad
5) Ensamblar los componentes en la base y armar la coraza. Para esto, guiarse por el archivo "ensamblado.f3z"
6) Asegurar todo en sus lugares, utilizar la máxima cantidad de tornillos sin llegar a dañar la madera
7) Comprobar que el circuito electrico funcione correctamente, guiarse a través de los diagramas
8) Ensamblar el arma a la coraza y unir esta parte con la base
10) Comprobar el funcionamiento de Kampfi con el diagrama funcional

Su Kampfi esta listo para funcionar.

**no nos hacemos responsables de fallas con las ruedas o daños ocasionados por el poco cuidado con el arma**

## Licencia
<a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/"><img alt="Licencia Creative Commons" style="border-width:0" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" /></a><br />Esta obra está bajo una <a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/">Licencia Creative Commons Atribución-NoComercial 4.0 Internacional</a>.

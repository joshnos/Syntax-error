# Detección de escenas de violencia
El presente proyecto pretende ser una alternativa que contribuya a mejorar la seguridad ciudadana, a través de un sistema que permita identificar hechos de violencia, lo cual podría ser utilizado para implementar un mecanismo de prevención y/o alerta ya que detecta escenas de violencia en videos, ya sean captados con camaras de vigilancia o tambien con grabaciones de celulares. 

## Syntax-error
Código del proyecto final para el Bootcamp para los Objetivos de Desarrollo Sostenible de HackCities desarrollado con Python.

## Motivación
La seguridad ciudadana es una de las mayores preocupaciones actualmente en el país, principalmente en las 3 ciudades principales de Bolivia: La Paz, Cochabamba y Santa Cruz, siendo una de las problemáticas más importantes el incremento de escenas de violencia. De acuerdo a una publicación realizada en el periódico “Página SIETE”, se menciona que, una encuesta de Ciesmori revela que ocho de cada 10 personas que viven en el eje troncal del país consideran que la seguridad ciudadana es un problema muy importante que afecta a todo el país. Los datos publicados en 2021 señalan que el 26% de los consultados fueron víctimas de agresiones en los últimos 12 meses, pero sólo el 31% de ellos hizo la denuncia ante las autoridades correspondientes. El 68% no la realizó.

En ese contexto, el presente proyecto pretende ser una alternativa que contribuya a mejorar la seguridad ciudadana, a través de un sistema que permita identificar hechos de violencia, lo cual podría ser utilizado para implementar un mecanismo de prevención y/o alerta, con el fin de reducir estos hechos que atentan contra la seguridad, tranquilidad y paz de las personas.

De esta forma, esta propuesta está enfocada en la ODS 16: Paz, justicia e instituciones sólidas, la cual busca reducir significativamente todas las formas de violencia y las correspondientes tasas de mortalidad en todo el mundo.

## Trabajos relacionados
La detección de violencia es un tema bastante estudiado en el campo de la vision artificial, ya que busca darle mas funcionalidad a las camaras de vigilancia, detectando escenas de violencia para un pronto actuar y disminuir el tiempo de respuesta ante estas situaciones. 
Por esto encontramos diferentes articulos cientificos los cuales presentan el uso de diferentes métodos para resolver este problema o hacerlo mas eficiente. 

Uno de los métodos mas utilizado es el de transferencia de aprendizaje usando redes convolucionales profundas. Este método es bastante utilizado dada la falta de un conjunto de datos amplio o suficientemente grande como para obtener los resultados esperados. Se utilizan diferentes modelos como ser YOLO, Inception y VGG_16. Pero también se encontró trabajos donde se proponen nuevos modelos como ser "FightNet" o por otro lado se encotrarón trabajos que comparan diferentes soluciones propuestas y crean un benchmark entre ellas.

## Métodos utilizados
Para la realización de este proyecto se utilizó el método de transferencia de aprendizaje usando redes convolucionales profundas, se propone utilizar el modelo Inception V3 con los pesos del conjunto de datos ImageNet, para entrenar el módelo se utilizó un conjunto de datos abierto, que se encuentra en la plataforma Kaggle. Este conjunto de datos cuenta con dos clases: Violence y Non-Violence con 1000 videos cortos en cada clase. Estos videos fueron recolectados de youtube.
Al iniciar el proyecto se hizo la prueba con diferentes modelos, los cuales eran: yolo_lite, mobileNet, VGG_16, ResNet101V2 y por último Inception V3. Se decidio usar Inception V3 dado que se obtenia el mayor nivel de precision con este modelo. 
Para entrenar nuestro modelo con nuestros datos se dividió el conjunto de datos en 2, entrenamiento y prueba, teniendo el conjunto de datos de prueba un 20% del total del conjunto de datos. 
El modelo fue entrenado utilizando ADAM como funcion de optimización, binary_crossentropy como función de pérdida y se usó el accuracy y el f1_score como métricas del entrenamiento.

## Resultados experimentales
El modelo fue entrenado varias veces, durante el proceso de Fine tunning de los hiperparametros. Como resultado de la métrica con el conjunto de prueba se obtuvo un 76% y un 80% en el conjunto de datos de prueba.

## Capturas de pantalla
Incluir logos o capturas de pantalla de las interfaces mas relevantes del proyecto.

## Tecnologías/Frameworks utilizados
- Python
- Keras
- Pytorch

## Funcionalidades mas importantes
Clasificación de videos que incluyen escenas de violencia o no.

## Instalación
El proyecto se debe trabajar en un ambiente de Python configurado para trabajar con tensorflow. Una vez clonado el proyecto se debe abrir el notebook con algún editor de texto o con Jupyter Notebooks, para luego ejecutar las celdas en orden. 

## Creditos
- Edson Segales
- Flavio Abdon
- Jasiel Renteria
- Joshua Nostas

## Licencia

The MIT License

Copyright (c) 2020 [nombre de equipo]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

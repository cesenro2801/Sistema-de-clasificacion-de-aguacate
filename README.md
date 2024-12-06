<h1 align='center'>SISTEMA DE CLASIFICACIÓN DE AGUACATES (INTELIGENCIA ARTIFICIAL 2)</h1><BR>

<h2>Planteamiento del Problema</h2>
<p>El aguacate Hass es la tercera fruta más exportada de Colombia. La clasificación precisa de su madurez tras la cosecha es esencial para mantener la calidad y reducir pérdidas. Este proyecto busca resolver este problema mediante técnicas de visión por computadora.</p>

<h2>Dataset</h2>

<h2><a href="https://data.mendeley.com/datasets/3xd9n945v8/1">'Hass' Avocado Ripening Photographic Dataset</a></h2>
<p>Este conjunto de datos consiste en 14.710 fotografías etiquetadas de aguacates Hass (Persea Americana Mill. cv Hass), redimensionadas a 800 x 800 píxeles y guardadas en formato .jpg, diseñadas para facilitar el desarrollo de modelos de aprendizaje profundo para predecir los estados de maduración y estimar la vida útil.

Un total de 478 aguacates Hass fueron adquiridos tres días después de la cosecha y categorizados en tres grupos de almacenamiento: T10 a 10 ºC con 85% de humedad relativa (HR); T20 a 20 ºC con 85% de HR; y Tamb en condiciones ambientales.

El proceso de maduración de estos aguacates se documentó mediante fotografías diarias (2 de cada muestra de lados opuestos), cada una vinculada a un Índice de Maduración detallado con cinco etapas: 
1 - Poco maduro;
2 - Rompiendo;
3 - Maduro (Primera Etapa);
4 - Madura (segunda fase);
5 - Sobremaduración.

La cuarta etapa marcaba el final de la vida útil de los aguacates, y cualquier muestra clasificada en la etapa 5 se consideraba pasada de madurez. Las marcas de tiempo de cada fotografía permiten hacer un seguimiento de la duración desde cualquier fotografía hasta el momento en que cada aguacate alcanzó el final de su vida útil.

Además, el conjunto de datos va acompañado de una hoja de cálculo Excel en la que figuran todos los nombres de archivo de las fotografías, su correspondiente número de muestra, el grupo de almacenamiento, la clasificación según el índice de maduración en 5 fases, el día en que se tomó la fotografía en relación con el inicio del experimento y el lado del fruto fotografiado (a o b).
</p>

<h2>Objetivo</h2>
<p>Desarrollar un algoritmo de inteligencia artificial que permita clasificar los aguacates Hass en las siguientes cinco etapas de madurez:</p>
<ol>
    <li>Poco maduro</li>
    <li>Roto</li>
    <li>Maduro (Primera Etapa)</li>
    <li>Maduro (Segunda Etapa)</li>
    <li>Sobremaduro</li>
</ol>

<h2>Procesamiento de Datos</h2>
<ul>
    <li><strong>Tamaño del conjunto de datos</strong>: 5000 imágenes (1000 por clase)</li>
    <li><strong>División de datos</strong>: 80% entrenamiento, 20% prueba</li>
    <li><strong>Técnicas aplicadas</strong>:
        <ul>
            <li>Conversión de etiquetas</li>
            <li>Normalización de datos</li>
        </ul>
    </li>
</ul>

<h2>Modelo de Procesamiento</h2>
<p>Se utilizó un modelo basado en <strong>ResNet-50</strong> preentrenado con ImageNet. Solo se entrenaron las capas integradas al modelo base, y posteriormente se realizó un fine-tuning, descongelando 30 capas adicionales.</p>

<h3>Arquitectura del Modelo:</h3>
<ul>
    <li><strong>Base</strong>: ResNet-50</li>
    <li><strong>Capas Adicionales</strong>:
        <ul>
            <li>Global Average Pooling</li>
            <li>Capa Densa (128 neuronas)</li>
            <li>Capa de salida (5 clases)</li>
        </ul>
    </li>
</ul>

<h2>Resultados</h2>
<ul>
    <li>Precisión en entrenamiento: <strong>0.91</strong></li>
    <li>Precisión en prueba: <strong>0.82</strong></li>
</ul>
<p>Los resultados muestran una mejora significativa gracias al fine-tuning. Futuras optimizaciones podrían incluir:</p>
<ul>
    <li>Incremento del conjunto de datos</li>
    <li>Ajustes en las capas descongeladas</li>
    <li>Refinamiento de la tasa de aprendizaje</li>
    <li>Implementación de técnicas de regularización</li>
</ul>

<h2>Índice del Proyecto</h2>
<ol>
    <li>Planteamiento del Problema</li>
    <li>Objetivo</li>
    <li>Procesamiento de Datos</li>
    <li>Modelo de Procesamiento</li>
    <li>Resultados</li>
</ol>

<hr>

<h2>Autor</h2>
<p>César Enrique Rojas Hernández</p>

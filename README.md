<h1 align='center'>SISTEMA DE CLASIFICACIÓN DE AGUACATES (INTELIGENCIA ARTIFICIAL 2)</h1><BR>

<h2>Planteamiento del Problema</h2>
<p>El aguacate Hass es la tercera fruta más exportada de Colombia. La clasificación precisa de su madurez tras la cosecha es esencial para mantener la calidad y reducir pérdidas. Este proyecto busca resolver este problema mediante técnicas de visión por computadora.</p>

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

Descripcion del contexto

Se incluyen todas las variables para poder probar los algoritmos que seleccionan o aprenden pesos para los atributos. Sin embargo, no se incluyeron atributos claramente no relacionados; se seleccionaron los atributos si había alguna conexión plausible con el crimen (N = 122), más el atributo que se predijo (Crímenes violentos per cápita). Las variables incluidas en el conjunto de datos involucran a la comunidad, como el porcentaje de la población considerada urbana y el ingreso familiar medio, e involucran a las fuerzas del orden público, como el número per cápita de agentes de policía y el porcentaje de agentes asignados a las unidades de drogas.

La variable de delitos violentos per cápita se calculó utilizando la población y la suma de las variables delictivas consideradas delitos violentos en los Estados Unidos: asesinato, violación, robo y asalto. Al parecer, hubo cierta controversia en algunos estados con respecto al recuento de violaciones. Estos resultaron en valores perdidos para la violación, lo que resultó en valores incorrectos para los delitos violentos per cápita. Estas ciudades no están incluidas en el conjunto de datos. Muchas de estas comunidades omitidas eran del medio oeste de Estados Unidos.

Los datos se describen a continuación en función de los valores originales. Todos los datos numéricos se normalizaron en el rango decimal 0,00-1,00 utilizando un método de agrupación de intervalos iguales no supervisado. Los atributos conservan su distribución y sesgo (de ahí que, por ejemplo, el atributo de población tenga un valor medio de 0,06 porque la mayoría de las comunidades son pequeñas). P.ej. Un atributo descrito como "media de personas por hogar" es en realidad la versión normalizada (0-1) de ese valor.

La normalización conserva proporciones aproximadas de valores DENTRO de un atributo (p. Ej., El doble del valor para el doble de la población dentro de la precisión disponible, excepto para los valores extremos (todos los valores más de 3 DE por encima de la media se normalizan a 1,00; todos los valores de más de 3 DE por debajo de la media está nromalizada a 0,00)).

Sin embargo, la normalización no preserva las relaciones entre los valores ENTRE atributos (por ejemplo, no sería significativo comparar el valor de whitePerCap con el valor de blackPerCap para una comunidad)

Una limitación fue que la encuesta LEMAS fue de los departamentos de policía con al menos 100 oficiales, más una muestra aleatoria de departamentos más pequeños. Para nuestros propósitos, se omitieron las comunidades que no se encuentran en los conjuntos de datos del censo y del crimen. A muchas comunidades les faltan datos de LEMAS.

Descripción del dataset
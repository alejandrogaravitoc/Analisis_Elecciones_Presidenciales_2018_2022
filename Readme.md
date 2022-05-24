# Proyecto Final de MCPP
## Realizado por Alejandro Garavito Carrascal

[Hoja de vida](https://github.com/alejandrogaravitoc/Analisis_Elecciones_Presidenciales_2018_2022/blob/main/CV/2022%20Hoja%20de%20Vida%20-%20Alejandro%20Garavito%20C%20(B-F)%20A2.pdf)

# Resumen y Motivación

Campaña tras campaña, candidatos presidenciales se presentan ante el público, les realizan entrevistas, dan debates, y responden preguntas del cómo serían de presidentes, enfocandose en el qué harían. Es por este motivo que en esta ocasión se estudiarán las entrevistas que han dado los tres candidatos más opcionados, y daremos una idea de sus propuestas principales, viendo aquellas que más hacen énfasis, su coherencia y continuidad a lo largo de los años, además del contexto en el que mencionan las mismas. 

Este estudio se dividirá en cuatro partes, una inicial, donde se estudiaran las palabras mencionadas de manera frecuente por los candidatos a través de entrevistas que se subieron a Youtube, tomando los subtitulos generados por esta plataforma. Una segunda parte, donde se agregan los insumos de la primera parte, de modo que se puedan analizar palabras clave mencionadas por el mismo candidato y se pueda comparar entre ellos cuál le da una mayor importancia a determinado factor. Una tercera parte, que aplica las bases de la inteligencia artificial aplicada al lenguaje humano para determinar que tan símiles son los discursos entre los candidatos y que tan constantes se mantienen con el discurso otorgado hace 4 años (o en el caso que no este el mismo candidato, qué tan constante se mantiene el discurso con el candidato de la misma rama ideológica). Finalmente, para concluir, en la cuarta parte se determina qué tan útil es este método de estudio, revisando los discursos que dió el presidente actual y comparandolo con lo que efectivamente realizó. 

Algunas de las preguntas que motivaron y fueron resueltas en este estudio fueron: 
* ¿Existe alguna forma de resumir puntos clave de las entrevistas a los candidatos sin la necesidad de escuchar las horas completas de los mismos? 
* Teniendo en cuenta sustentos en la psicología, ¿Cuáles son las palabras que más se repiten, que vendrían a ser las que más identifican a cada candidato, a lo largo de las entrevistas?
* ¿Podemos generar algún tipo de indicador que compare aquellas palabras que más se repiten entre los diferentes candidatos?
* Teniendo en cuenta que más allá de las palabras mencionadas, tendrá relevancia el contexto de las mismas ¿podríamos obtener el contexto de alguna palabra en específico de cada uno de los candidatos?
* ¿Cómo ha cambiado el discurso del candidato Petro o Fajardo a lo largo de estas dos elecciones? 
* ¿Qué tan parecido es el discurso entre candidatos?
* ¿Realmente el discurso de Federico Gutiérrez es similar al de Iván Duque?
* ¿Qué tan útil puede ser esta herramienta de análisis?, ¿los candidatos mienten o hace falta escuchar o leer entre lineas de lo que mencionan para saber sus verdaderos planes durante la campaña?  

---
---

# Métodos utilizados

1. Scrape-transcripts de YouTube
* Como la idea es que las personas puedan efectuar este tipo de estudios en un futuro, se deja el espacio donde se le solicitará a la persona que ingrese 3 links de las entrevistas de los 3 candidatos más votados, puede ingresar hasta 3 entrevistas diferentes, el programa hará el resto del trabajo, tomando los subtitulos de las mismas y llevando al análisis requerido. En esta ocasión, para darle fluidez al código se dejarán preestablecidos los links de las entrevistas.
* Es importante tener en cuenta que para este estudio se deben tomar el mismo esquema de entrevistas, de modo que sean lo más comparables que se pueda. Esto, pues, se debe ser consciente que, dependiendo del entrevistador se guiara el dialogo por diferente camino. Sin embargo, no deja de haber un discurso claro dentro de la campaña de cada candidato el cual tenemos la tarea de revelar.
* Este estudio se basa en Bargh (2007) el cual nos menciona que las personas automáticamente generamos procesos mentales que se reflejan de manera inconsciente en nuestras actitudes o, en este caso, en lo que mencionamos. De este modo, puede que a una persona le pregunten por datos diferentes que a otra, sin embargo, siempre esta encaminará las respuestas a sus propuestas e ideas, y enfatizará en las que esten más cercanas a sus ideas (el énfasis se verá reflejado en el número de veces que se repite una palabra). Bibliografía: Bargh, J. A. (Ed.). (2007). Social psychology and the unconscious: The automaticity of higher mental processes. Psychology Press.
* Para esta coyuntura presidencial, se generaron diversos tipos de entrevista, etre las cuales rescataremos tres:
    * El Espectador, esta haciendo un trabajo periodistico de gran valor y calidad, que es poner a los candidatos a exponer sus propuestas.
        * Entrevista Gustavo Petro 7 de Dicimbre 2021 https://www.youtube.com/watch?v=6gr8mLIEdh0
        * Entrevista Sergio Fajardo 17 de Noviembre https://www.youtube.com/watch?v=-wRzFes7ToY
        * Entrevista Federico Gutierrez 24 de Febrero 2022 https://www.youtube.com/watch?v=OOGPU2JbVwI
    * El periódico la República, hace un trabajo similar al previamenete planteado, sin embargo, esta mucho más enfocado que el del Espectador a temas económicos.
        * Entrevista Gustavo Petro, 9 de Marzo 2022, https://www.youtube.com/watch?v=Ii4vOY9jFdQ
        * Entrevista Sergio Fajardo 1 de Abril del 2022, https://www.youtube.com/watch?v=Kk2tGDtzlvo
        * Entrevista Federico Gutierrez, 22 de Febrero 2022, https://www.youtube.com/watch?v=9Z8O0riVLhM
    * El país de los jóvenes, aunque es más sesgado que el anterior, en tanto los entrevistadores tomaran temas algidos de la campaña, esto mismo puede hacer que el estudio de lo mencionado sea interesante. Especialmente considerando que el candidato es quien termina hablando gran parte del debate.
        * Entrevista Gustavo Petro, 28 de Abril de 2022, https://www.youtube.com/watch?v=fMlqcIL0toc
        * Entrevista Sergio Fajardo, 26 de abril 2022, https://www.youtube.com/watch?v=HXIikDcEijI
        * Entrevista Federico Gutierrez, 25 de Abril 2022, https://www.youtube.com/watch?v=e4HtLgb88f0


2. Estudio de ideas principales:  
* Con base en el estudio de psicología previamente mencionado, se hará un estudio de las palabras más mencionadas, gráficandolas tanto a través de Nubes de Palabras como de gráficos de barras de frecuencia de las mismas. 
* Así mismo, se revisará el contexto en el que fueron mencionadas dichas palabras que se necesiten estudiar o que se consideren pertinentes. 
* Se genera un indicador que permite la comparación de diferentes palabras entre discursos presidenciales. 

3. NPL - Inteligencia Artificial aplicada al lenguaje humano:
    
* Con base en uno de los discursos presidenciales, en este caso, por tener una estructura muy similar entre entrevistas se elige la del "Diario la República". Se hace un análisis de Vector TF-IDF y de similaridad del coseno entre vectores para la comparación de los discursos de cada uno de los candidatos presidenciales, que en palabras normales es un análisis de correlación entre discrusos que tiene en cuenta regularidad de una palabra, tanto en el discurso como entre discursos, saca una métrica de valoración de palabras, convierte el discruso en un vector numérico y así con la similitud del coseno (medida de similaridad entre dos vectores) podemos hallar "la correlación" entre diferentes discursos.  
* Para hacer más interesante este análisis entre discursos, se evaluan 3 nuevas entrevistas realizadas por el "Diario La República" hace 4 años en los debates de las pasadas elecciones. Aquí se analizará adicionalmente el discurso de Ivan Duque ante la inexistencia de Feredico Gutierrez en las anteriores candidaturas presidenciales y el querer observar qué tanto varian ambos discursos, teniendo en cuenta que hacen parte de un mismo sector ideológico. 
    * Por Gustavo Petro, el 19 de Febrero del 2018: https://www.youtube.com/watch?v=pxyQ6bZsZho
    * Por Sergio Fajardo,  el 1 de Marzo 2018: https://www.youtube.com/watch?v=sVvmWL-hRsg
    * Por Ivan Duque, el 15 de Febrero del 2018: https://www.youtube.com/watch?v=vWtLLk9dXOs

4. Utilidad de esta herramienta: 
* Para evaluar la utilidad de esta herramienta generada, tomamos el discurso de Ivan Duque 2018, de modo que a través de uno de los lemas más mencionados de su campaña "Menos impuestos, más salarios" y a través de la entrevista previamente mencionada, podamos responder la pregunta de si mintió o no se escucho entre lineas o detalladamente lo que él decía. Para hacer este análisis se reutilizarán los métodos previamente explicados. 

---
---

# Resultados: 

Todos los análisis aquí planteados, gráficos generados y demás, pueden ser replicados a través de este [código](https://github.com/alejandrogaravitoc/Analisis_Elecciones_Presidenciales_2018_2022/blob/d747b2a8fcfd1caa5999088d3a9048834d6921d6/Co%CC%81digo/Proyecto_Final_Garavito_Alejandro_1.ipynb)

Las siguientes 3 gráficas muestran las nubes de palabrasde las 3 entrevistas que se realizaron a cada uno de los candidatos. De estas podemos observar similitudes, diferencias, y detalles del discurso que podría ser interesante mejorar en caso que uno quiera utilizar esta herramienta como insumo para ser el director de debate del candidato. 

Por ejemplo, observemos como Gustavo Petro y Federico Gutierrez (Fico) han incluido en sus discursos materias de género, sin embargo, el primero tiene un enfoque más social, en tanto el segundo, aunque da visos de oportunidades enfocados en la educación, se enfoca más en la empresa y la inversión. Por su parte, Fajardo tiene un discurso más enfocado a los territorios, la violencia y las comunidades (teniendo en común con Fico, su insistencia en la educación). 

Por otro lado, se pueden denotar temas relevantes tomados por los candidatos, para dar una imagen de esto, se puede observar la entrevista de la República, donde Petro habla de pensiones y de petroleo, Fajardo de desarrollo y personas, y Fico de empresas y gente.  

Finalmente, podemos observar como se repiten constantemente en discursos de Fajardo y de Fico palabras como "creo", palabras que pueden restarle credibilidad a un discursos, de modo que, esta herramienta también podría ser utilizada por un director de debate, redireccionando discursos o eliminando muletillas. 

![Captura%20de%20Pantalla%202022-05-24%20a%20la%28s%29%204.33.35%20p.m..png](attachment:Captura%20de%20Pantalla%202022-05-24%20a%20la%28s%29%204.33.35%20p.m..png)

![Captura%20de%20Pantalla%202022-05-24%20a%20la%28s%29%204.33.46%20p.m..png](attachment:Captura%20de%20Pantalla%202022-05-24%20a%20la%28s%29%204.33.46%20p.m..png)

![Captura%20de%20Pantalla%202022-05-24%20a%20la%28s%29%204.33.57%20p.m..png](attachment:Captura%20de%20Pantalla%202022-05-24%20a%20la%28s%29%204.33.57%20p.m..png)

## Estudio de ideas principales:

Las entrevistas previame transcritas se van agregando, para este estudio de ideas, de modo que podemos observar ya sea a través de la nube de palabras vistas previamente o a través del siguiente gráfico, cuáles son las palabras más mencionadas y cuál podríamos analizar más al detalle. Es más una herramienta que una conclusión de este ejercicio. 

![Captura%20de%20Pantalla%202022-05-24%20a%20la%28s%29%204.54.17%20p.m..png](attachment:Captura%20de%20Pantalla%202022-05-24%20a%20la%28s%29%204.54.17%20p.m..png)

Otra de las herramientas generadas da la posibilidad de comparar palabras a través de un indicador. Este indicador tomará el número de veces que se menciona una palabra sobre el total de las palabras relevantes mencionadas por cada uno de los candidatos. Esto le permitirá al usuario, medir la relevancia de un tema para cada uno de los candidatos. En este caso, observamos como, por ejemplo, las oportunidades son prioridad para Fico y Fajardo, en tanto, temas como las pensiones, el hambre el metro, son de prioridad mayor para Petro. 

![Captura%20de%20Pantalla%202022-05-24%20a%20la%28s%29%205.03.39%20p.m..png](attachment:Captura%20de%20Pantalla%202022-05-24%20a%20la%28s%29%205.03.39%20p.m..png)

Finalmente en esta sección, podemos observar como contamos con la última herramienta, que nos es útil para realizar el análisis de contexto. Como ejemplo, tomamos al candidato 1, que es Gustavo Petro, y pusimos que queríamos ver el contexto de cuando menciona impuestos. De estas frases podemos concluir que: 
1. Los gastos aumentaron, se produjo déficit, se disminuyeron los ingresos, de modo que es necesaria una reforma tributaria. A lo que pregunta ¿quién va a pagar por los impuestos? Carrasquilla propuso ponerle impuestos comida, de modo que el candidato propone derogar reforma tributaria de 2019 la cual aumenta el déficit.
2. Necesidad de impuestos a los dividendos, teniendo en cuenta el nivel de evasión y elusión de los altos ingresos. 
3. Impuesto empresas extractivas.
4. Impuestos a los más ricos

Es muy interesante llegar a estos análisis sin tener que escuchar 3 horas de entrevista. Este discurso así mismo, podemos determinar que es coherente con su rama ideológica. 

![Captura%20de%20Pantalla%202022-05-24%20a%20la%28s%29%205.21.35%20p.m..png](attachment:Captura%20de%20Pantalla%202022-05-24%20a%20la%28s%29%205.21.35%20p.m..png)

---
---

## NPL - Inteligencia Artificial aplicada al lenguaje humano:

Como se mencionaba previamente, con base en las entrevistas del "Diario la República" tanto del 2018 como del 2022. Se hace un análisis de Vector TF-IDF y de similaridad del coseno entre vectores para la comparación de los discursos de cada uno de los candidatos presidenciales. En palabras normales es un análisis de correlación entre discrusos que tiene en cuenta regularidad de una palabra, tanto en el discurso como entre discursos, saca una métrica de valoración de palabras, convierte el discruso en un vector numérico y así, con la similitud del coseno (medida de similaridad entre dos vectores), podemos hallar "la correlación" entre diferentes discursos.

Con esta herrramienta, la cual arroja el resultado de la imagen citada posteriormente, podemos afirmar que el discurso de los candidatos ha permanecido básicamente constante a lo largo del tiempo, incluido el de Federico Gutierrez (2022) con el candidato de ideología similar Ivan Duque (2018). Así mismo, podemos ver cierta similitud entre candidatos, especialmente, entre el discurso de Ivan Duque (2018) y Fajardo (2018), discurso que este último ha venido diferenciando de los demás. 

![Captura%20de%20Pantalla%202022-05-24%20a%20la%28s%29%205.34.46%20p.m..png](attachment:Captura%20de%20Pantalla%202022-05-24%20a%20la%28s%29%205.34.46%20p.m..png)

## Utilidad de las Herramientas: 


    ¿Qué tanto sirve realizar este análisis? Teniendo en cuenta que los candidatos puededn mentir, podemos tomar una de las entrevistas que le hicieron al candidato Ivan Duque (actual presidente de Colombia) de hace 4 años, y hacer un análisis no exaustivo (hacerlo exhaustivamente es una investigación pendiente para trabajos futuros) de si cumplió alguna de sus propuestas, reflejadas en las palabras más mencionadas o no.  

![Duque.png](attachment:Duque.png)

Vemos a través del gráfico de Nube de Palabras como se resaltan palabras como: 
* Impuesto 
* Empresa
* Mercado
* Inversión 
* Reforma tributaria

A lo que la pregunta a resolver es, ¿se podría predecir con estos análisis cual era la verdad detrás de la frase de las vallas que decian "más salarios, menos impuestos"?

![Duque_valla.jpeg](attachment:Duque_valla.jpeg)

Con las herramientas vistas previamente, podemos acercarnos al qué se refería con esta afirmación. 
En el siguiente caso, vamos a llenar, "impuesto", "500" (para obtener 500 caracteres a lado y lado de la palabra impuestos y de esta forma obtener el contexto de la misma), y "3" (que fue el número del candidato elegido para esta última parte). 


```python
pregunta=input("¿Qué palabra quisiera ver el contexto? (es irrelevante si usa mayuscula o minúscula, es relevante la ortografía y si esta en singular o en prural, sugerimos por eso basarse en las nubes de palabras): ")
while True:
    try:
        carac=input("¿Cuántos carácteres quisiera ver a lado y lado de la palabra (sugerencia 500): ")
        break
    except ValueError: 
        print("Ingrese un número entero por favor")

num_c=input("¿De cuál de los candidatos? Ponga: 1,2 o 3: ")
while not (num_c=="1")|(num_c=="2")|(num_c=="3"): 
    print("Número de candidato no válido")
    num_c=input("¿De cuál de los candidatos? Ponga: 1,2 o 3: ")
    
pregunta=pregunta.lower()
tokens = nltk.word_tokenize(locals()["sub_e4_"+str(num)])
text = nltk.Text(tokens)
lista=text.concordance(pregunta, width=500)
# Sugerencia: Impuesto, 500, 3 (Pues queremos analizar a Duque)
```

    ¿Qué palabra quisiera ver el contexto? (es irrelevante si usa mayuscula o minúscula, es relevante la ortografía y si esta en singular o en prural, sugerimos por eso basarse en las nubes de palabras): impuesto
    ¿Cuántos carácteres quisiera ver a lado y lado de la palabra (sugerencia 500): 500
    ¿De cuál de los candidatos? Ponga: 1,2 o 3: 3
    Displaying 8 of 8 matches:
    me lleva a otras propuestas por ejemplo hay que quitarle el iva a los bienes de capital porque se tiene que ayudar tenemos que ayudar a que se de la reconversión industrial a que haya una reconversión tecnológica y me parece que tal como está el impuesto hoy es incentivar esos procesos tercero yo creo que el impuesto a los dividendos como está planteado hoy me parece que genera mucha disuasión para el desarrollo de mercados de capital y tienen muy poco recaudo tenemos un país con menos de 80 emp
    a los bienes de capital porque se tiene que ayudar tenemos que ayudar a que se de la reconversión industrial a que haya una reconversión tecnológica y me parece que tal como está el impuesto hoy es incentivar esos procesos tercero yo creo que el impuesto a los dividendos como está planteado hoy me parece que genera mucha disuasión para el desarrollo de mercados de capital y tienen muy poco recaudo tenemos un país con menos de 80 empresas listadas en bolsa solamente cinco empresas están transando
     genera mucha disuasión para el desarrollo de mercados de capital y tienen muy poco recaudo tenemos un país con menos de 80 empresas listadas en bolsa solamente cinco empresas están transando más de cinco millones al día y me parece que tener el impuesto a los dividendos distrae lo que debería ser el desarrollo de mercados de capital y tiene muy poco impacto al recaudo y otra propuesta que nosotros hemos planteado en cuanto al iva tenemos un iba con una tarifa muy alta y tenemos unida profundame
    en términos de impuestos porque va a hacer una reducción y lo va a compensar con un estado claro mucho más delgado pero me falta una cosa que tengo que decirle a usted que es donde está la principal reducción hoy nosotros tenemos una evasión del impuesto de renta y de iva que puede prácticamente superar los 40 billones de pesos al año la meta que nosotros debemos fijarnos en los próximos cuatro años como mínimo es reducirla en un 50 % cómo se puede reducir una de las tareas es profundizar la fac
    ivar la economía en primer lugar yo creo que hay que bajar rentas corporativas sobre todo y por otro lado yo creo que se puede buscar una combinación de reducir algunas tarifas de iva a unos puntos en la tarifa arriba y aumentar la cobertura del impuesto dejen una frasecita usted vio lo que pasó en eeuu la semana pasada el gobierno de eeuu bajo impuesto de renta y una empresa como wall mart que es el principal empleador de los eeuu mejoró la remuneración de los trabajadores si usted me pregunta 
    lado yo creo que se puede buscar una combinación de reducir algunas tarifas de iva a unos puntos en la tarifa arriba y aumentar la cobertura del impuesto dejen una frasecita usted vio lo que pasó en eeuu la semana pasada el gobierno de eeuu bajo impuesto de renta y una empresa como wall mart que es el principal empleador de los eeuu mejoró la remuneración de los trabajadores si usted me pregunta a mí la combinación debe ser bajar impuestos con un estado a usted incentivar la inversión y mejorar 
    omo fueron los fondos yosman israel que ayudaron con capital semilla y yo pienso una cosa fernando nosotros necesitamos que para el primer emprendimiento en colombia tengamos facilidades yo creo que colombia necesita por ejemplo una exención del impuesto de renta por cinco años para nuevos negocios que generen un mínimo de puestos de trabajo pero que estén orientadas en actividades de valor agregado en tecnología por ejemplo computación en la nube inteligencia artificial big data block change y 
    ficientes hoteles para no ser para no ser de pronto de no ser proporcional y aquí se necesitaba generar mucha más infraestructura hotelera que a su vez tiene un gran impacto en la generación de empleo formal que se hizo se busca una exención del impuesto de renta por 30 años y una ciudad como cartagena duplicó su base hotelera generando empleos en el sector si nosotros queremos llevar empleos formales al campo yo creo que nosotros deberíamos tener una exención de impuestos de renta por 10 años a


Podemos observar varios puntos: 
1. Quitar IVA bienes de Capital.
2. Modificar impuestos a los dividendos.
3. Evasión impuesto de renta IVA
4. Evaluar reducir tarifa de IVA y aumentar la cobertura de dicho impuesto. 
5. Bajar rentas corporativas (basandose que en EEUU luego de hacer esto Walmart subió sus salarios). 
6. Excención impuesto de renta hoteles. 

En ninguna parte se veía la palabra equidad, de modo que, políticas como "modificar impuestos a los dividendos", que son políticas que benefician a las personas más ricas del país, exactamente al 1% más rico (Londoño y Joumard, 2013) son congruentes con lo que él venía proponiendo. Así mismo, efectivamente se puede observar que cumple con sus promesas de campaña al reducir impuestos a las empresas. Lo cual nos indica que no es que haya dicho mentiras, sino que hay que leer entre lineas de lo que proponen los candidatos. Así mismo, podemos ver que desde su discurso inicial mencionaba la opción de aumentar la cobertura del impuesto de IVA. 

Por otro lado, respecto la parte de la valla que mencionaba "más salarios", podemos decir que fue otra propuesta cumplida, pues, como veremos en el siguiente gráfico, generó el mayor incremento del salario mínimo que se ha visto en las últimas décadas (observando el incremento del salario real desde 1985). 

De modo que, si, esta herramienta es efectiva para analizar cuáles podrían ser los verdaderos intereses y lo que realmente harán los candidatos ante propuestas generales. 


```python
%%HTML

<div class='tableauPlaceholder' id='viz1653246658454' style='position: relative'><noscript><a href='#'><img alt='Dashboard 1 ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Pr&#47;Proyecto_MCPP&#47;Dashboard1&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='Proyecto_MCPP&#47;Dashboard1' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Pr&#47;Proyecto_MCPP&#47;Dashboard1&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='es-ES' /><param name='filter' value='publish=yes' /></object></div>                <script type='text/javascript'>                    var divElement = document.getElementById('viz1653246658454');                    var vizElement = divElement.getElementsByTagName('object')[0];                    if ( divElement.offsetWidth > 800 ) { vizElement.style.minWidth='1020px';vizElement.style.maxWidth='1920px';vizElement.style.width='100%';vizElement.style.minHeight='587px';vizElement.style.maxHeight='887px';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';} else if ( divElement.offsetWidth > 500 ) { vizElement.style.minWidth='1020px';vizElement.style.maxWidth='1920px';vizElement.style.width='100%';vizElement.style.minHeight='587px';vizElement.style.maxHeight='887px';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';} else { vizElement.style.width='100%';vizElement.style.height='727px';}                     var scriptElement = document.createElement('script');                    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                </script>
```



<div class='tableauPlaceholder' id='viz1653246658454' style='position: relative'><noscript><a href='#'><img alt='Dashboard 1 ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Pr&#47;Proyecto_MCPP&#47;Dashboard1&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='Proyecto_MCPP&#47;Dashboard1' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Pr&#47;Proyecto_MCPP&#47;Dashboard1&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='es-ES' /><param name='filter' value='publish=yes' /></object></div>                <script type='text/javascript'>                    var divElement = document.getElementById('viz1653246658454');                    var vizElement = divElement.getElementsByTagName('object')[0];                    if ( divElement.offsetWidth > 800 ) { vizElement.style.minWidth='1020px';vizElement.style.maxWidth='1920px';vizElement.style.width='100%';vizElement.style.minHeight='587px';vizElement.style.maxHeight='887px';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';} else if ( divElement.offsetWidth > 500 ) { vizElement.style.minWidth='1020px';vizElement.style.maxWidth='1920px';vizElement.style.width='100%';vizElement.style.minHeight='587px';vizElement.style.maxHeight='887px';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';} else { vizElement.style.width='100%';vizElement.style.height='727px';}                     var scriptElement = document.createElement('script');                    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                </script>



![Tableau.png](attachment:Tableau.png)

-----

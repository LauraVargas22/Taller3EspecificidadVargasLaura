**TALLER DE ESPECIFICIDAD**
Mediante la elaboración de este trabajo se busca comprender la funcionalidad de especificidad en CSS.

1. **Parte 1: Introducción teórica a la especificidad**
    En esta se evaluaron conceptos claves en la temática tales como: especificidad, tipos de selectores, valores de especificidad según el tipo de selector y la regla (!important). Por lo que se realizaron las siguientes diapositivas https://docs.google.com/presentation/d/13HzbAxWkbOnRjkP3V984eZFZycE4HkbM9XCv9y4pkU8/edit?usp=sharing

2. **Parte 2: Ejemplos Prácticos**
    En el primer ejercicio básico se reconoció la prevalencia en la aplicación de las reglas de estilo según el tipo de selector, como lo muestra el ejemplo a continuación:

        <div class="container">
            <p id="parrafo">Hola Mundo</p>
        </div>

    Según lo anterior, se aplicaron algunas reglas de estilo las cuales fueron:

        /*Parte 2 */
        p {
            color: blue; /* Valor de especificidad 1 por el tipo de selector elemento */
        }

        .container p {
            color: green; /* Especificidad = 11 (10 tipo de selector clase + 1 tipo de selector elemento)  */
        }

        #parrafo {
            color: red; /* Especificidad 100 por el tipo de selector ID, el cual tiene prioridad sobre los anteriores.*/
        }

    Por lo que, obtuvimos como resultado el texto en color ROJO al tener mayor valor de especificidad el ID parrafo.

    En el segundo ejercicio, hicimos uso de la regla !important de está manera:

        /*Parte 2 */
        p {
            color: blue !important; /*Al añadir !important no se tiene en cuenta el valor de especificidad, teniendo prevalencia esta regla de estilo */
        }

        #parrafo {
            color: red; /* Especificidad 100 por el tipo de selector ID, el cual tiene prioridad sobre los anteriores. Aunque la especificidad se ve afectada al encontrar un !important el cual da prioridad al tipo de selector elemento*/
        }

    Teniendo como resultado el texto AZUL pues la regla !important da prevalencia al selector elemento.
    




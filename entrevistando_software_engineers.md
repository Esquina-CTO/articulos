# Entrevistando Ingenieros de Software

De manera concisa, me gustaría presentarles algunos retos que he aplicado al momento de entrevistar candidatos, y también otros interesantes que me han aplicado, los cuales he visto como interesantes y que creo ayudan a evaluar candidatos de manera holística.

## 1. Code Review Interview
### Reto
Asignar una pieza de código al candidato para que realice una evaluación a sus criterios propios.

### Dinámica de entrevista
- El entrevistado adquiere un bloque de código que necesita revisar (normalmente en malas condiciones, incluso sin funcionar), y el candidato debe dejar comentarios a través de alguna herramienta como Github, Gitlab, o algúna herramienta de documentos que permita capturar comentarios. 
- El candidato tiene un tiempo limitado para dejar comentarios al respecto del código
- Ambas partes después empiezan a dialogar respecto a los comentarios, y a indagar en el por qué de estos.

### Criterios de evaluación
- Legibilidad de código
- Mejoras de performance
- Evaluación de casos esquina en el código
- Simplificación de código
- Estílo de código (atención al detalle en cuanto a formato de código o linting)
- Detección de vulnerabilidades (llaves privadas en el código, inyección de código SQL, etc.)
- Maneras de dar feedback del código

### Ventajas de esta entrevista
- Se puede profundizar en cuanto a conocimientos técnicos dependiendo del código a evaluar.
- Se detecta rápidamente el interés por revisar código y la experiencia haciéndolo
- Se pueden identificar sesgos no deseados u actitudes respecto a maneras de hacer código.

### Desventajas
- El código podría estar en un lenguaje en el que el candidato no se sienta tan cómodo
- La herramienta de revisión de código puede ser una barrera si el candidato no es capaz de utilizarla (ejemplo, el código está en github y el candidato no tiene cuenta).

### Ejemplo
[Code Review Exercise](https://www.notion.so/Code-Review-Exercise-d3508df54aec40419b16f105aaea8689)

### Notas
Este challenge me ha parecido bastante útil como primera entrevista. Se puede medir muchísimas cosas en un tiempo muy corto, y también puedes notar las actitudes del candidato respecto a código no tan limpio, y pedirle que profundice en cómo mejorar una solución ya implementada.

## 2. Entrevista de código usando pruebas unitarias
### Reto
Crear un modulo que pase ciertas pruebas automatizadas desarrolladas por el mismo candidato.

### Dinámica de entrevista
- Se entrega una pieza de código con un suite de pruebas automátizadas a través de una plataforma que pueda correr pruebas en la nube, o en la máquina del candidato (ejemplo, un link a algún [jsfiddle](https://jsfiddle.net/opensas/3VuGs/))
- El candidato empieza a hacer que las pruebas automatizadas pasen.
- Se le pide al candidato que realice más casos de prueba y vaya haciendo que pasen.
- Se le pide al candidato cómo podría refactorear el código para mejorar la calidad.

### Criterios de evaluación
- Legibilidad de código
- Desarrollo de casos de prueba
- Adopción de pruebas automatizadas

### Ventajas
- Se puede leer el nivel de expertise de un candidato por cómo escribe sus pruebas.
- Se puede evaluar qué tan bien el candidato puede refactorear su código y las decisiones que tome.

### Desventajas
- El código y pruebas podrían estar en un lenguaje en el que el candidato no se sienta tan cómodo

### Ejemplos
- _Desarrollar el módulo de compra de videojuegos en un sistema tipo Steam_. [link](https://jsfiddle.net/mhf8oubg/2/)
- _Desarrollar el modulo de compra de propiedades en un Monopoly_
- _Desarrollar el algoritmo para verificar el ganador de un juego de gato_

### Notas
Este reto permite descubrir cómo un candidato aborda un problema de diseño de software, y ayuda también a medir la capacidad de evaluar casos esquina en código, lo cuál es un mindset que considero que todos los ingenieros deben de tener muy presente.

## 3. Take-home challenge
### Reto
Desarrollar un subsistema en Front End y/o Back End con código parecido a producción

### Dinámica de entrevista
- Se manda un reto técnico a un candidato para desarrollar alguna aplicación definida bajo un tiempo específico (4-8 horas en una semana). Para los retos que involucran front end, puede ser buena idea mandar un set de mock ups para que el desarrollador tome como base.
- Posteriormente, agendar revisión del reto técnico con el candidato.
- Se hace una profundización en la solución planteada y se hacen preguntas de ambos lados.

### Criterios de evaluación
Dependiendo del tipo de reto, se puede evaluar lo siguiente:
- Abstracciones en código (Diseño de software)
- Manejo de credenciales (variables de ambiente)
- Conocimiento de pruebas automatizadas
- Conocimiento de frameworks de desarrollo
- Limpieza en código
- Manejo de trade-offs (por el límite de tiempo)
- Calidad en la funcionalidad del sistema
- Facilidad de correr el sistema.

### Ventajas
- Mucha profundidad en detalles de cómo es el trabajo de un candidato fuera del ambiente de entrevistas

### Desventajas
- Si un candidato no está realmente interesado en la empresa, puede que no realice el reto técnico.
- Dar feedback del reto técnico puede ser muy costoso en tiempo.
- Muchas horas invertidas del lado del candidato.

### Ejemplos
- Diseñar una interfaz web para desplegar una lista de Pokemons
- Diseñar un back end para verificar la cuenta de un usuario mediante un código SMS

### Notas
Personalmente, este reto es el que más me gusta aplicar, pero entiendo que es el más pesado y no es posible aplicarlo siempre, sobre todo si el candidato está entrevistando en otras 4 empresas, puede resultar bastante pesado.

## 4. Examen automatizado a traves de un Public API
### Reto
El candidato debe mandar requests a un API público para pedir información, transformarla, y regresarla procesada en un tiempo limitado.

### Ejemplo
Hacer peticiones a un API pública para que regrese un número específico del 1 al 100, y en base a ese número, regresar el número en la serie de fibonacci que pertenezca a la posición dada. Ejemplo:
```
GET /fibonacci
Response: 5
```
0 1 1 2 3 <- 5 8
```
POST /fibonacci
Data: { number: 3 }
Response: 2 # aquí la respuesta seria el siguiente número a buscar en la serie
```
0 1 <- 1 2 3 5 8
```
POST /fibonacci
Data: { number: 3 }
Response: 9 # y así sucesivamente hasta que el sistema determine que la entrevista ha terminado
```

### Dinámica de entrevista
- Se le entrega al candidato un API Key específico
- El candidato manda un primer request para empezar el challenge, y a partir de ahí el tiempo es limitado para resolver el reto.

### Criterios de evaluación
- Experiencia con tecnologías web

### Notas
Este reto se me hizo muy interesante cuando apliqué como intern a una empresa en el 2015, la verdad desconozco qué herramienta se utilizó por detrás, pero se me hizo un buen ejercicio para agarrar candidatos con algo de experiencia con web

## 5. Algoritmia
### Reto
Resolver un problema de algoritmia a un candidato y resolverlo en un tiempo limitado

### Dinámica de entrevista
- El candidato recibe un reto de algoritmos y se le pide que resuelva el problema con la solución más eficiente posible en cuanto a complejidad algorítmica, tomando en cuenta la notación Big-O

### Criterios de evaluación
- Pensamiento lógico del candidato
- Performance del algoritmo
- Limpieza de código

### Ventajas
- Filtro rápido de entrevista
- Muchas empresas utilizan este método como primera entrevista técnica, incluso se puede automatizar utilizando herramientas como [HackerRank](https://www.hackerrank.com/)

### Desventajas
- Puede no ser de interés para muchos entrevistadores
- Los candidatos suelen tener sentimientos no positivos respecto a estas entrevistas.

### Notas
Se me hace un método válido para evaluar si un candidato se siente cómodo con su lenguaje de programación y tiene un pensamiento lógico respecto a estructuras de datos y problemas complejos. Y como siempre, aplicar este tipo de entrevistas es circunstancial y subjetivo :P
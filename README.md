# AC-OPF-With-SOCP-Relaxation
Solving Multiperiod OPF Problems using an AC-QP Algorithm Initialized with an SOCP Relaxation
Credits to Jennifer F. Marley, Daniel K. Molzahn, and Ian A. Hiskens

Métodos para resolver AC OPF:
1. Newton
2. Programación Cuadrática Sucesiva (AC-QP)
3. Punto Interior

Si bien el flujo DC es mucho menos costoso computacionalmente puede brindar soluciones no factibles. El método de este paper utiliza linealizaciones sucesivas. Cada iteración del método AC-QP resuelve un flujo AC. 
Este método tiene la desventaja de depender del punto de inicialización teniendo como riesgos encontrar un óptimo local en lugar de uno global o no converger. Por lo tanto se requiere un método que permita encontrar buenos puntos de inicialización. Estos métodos relajan el problema original y permiten identificar límites inferiores de las soluciones óptimas, en algunos casos, estas soluciones pueden ser exactas. Los métodos comunes de relajo son SDP (semi-definite programming) y SOCP (Second-order cone programming), donde el segundo de ellos no tiene problema en ser aplicado a redes grandes. 

La necesidad de resolver un flujo AC multiperiodo tiene que ver con capturar las ventanas de tiempo asociada a las tecnologías de generación renovable y almacenamiento. 

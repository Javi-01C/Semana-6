


# COMPRENDE-1:

Cuando hago un `enqueue(X)` en una cola con lista enlazada que ya tiene 3 nodos:
- ESTADO ANTES: El puntero `frente` apunta al Nodo 1 que es el primero en salir.
                 El puntero `final` apunta al Nodo 3 que es el último que llegó. El `siguiente` del Nodo 3 apunta a null.
            
- ESTADO DESPUÉS: Primero creo el nuevo Nodo X. Luego, hago que la flecha (`siguiente`) del Nodo 3 apunte al nuevo Nodo X para enlazarlo a la cadena.
                Finalmente, muevo mi puntero `final` para que ahora apunte oficialmente al Nodo X. El puntero `frente` no se toca, sigue en el Nodo 1.

---

# COMPRENDE-2:

En una cola circular con arreglos, al unir el final con el principio, el estado "totalmente vacía" y "totalmente llena" pueden hacer 
que los punteros coincidan en la misma posición, confundiendo a la computadora. 
Para resolver esta ambigüedad, la forma más práctica es llevar una variable extra llamada `contador`. 
Así, si los punteros se cruzan pero `contador == 0`, sé que está vacía; y si `contador == capacidad máxima`, sé que está llena. 

---

# COMPRENDE-3:

Una cola FIFO simple en un hospital sería un desastre porque atiende por orden cronológico.
Si a las 8:00 AM llega alguien con un resfriado leve y a las 8:05 AM llega una persona con un infarto, 
una cola FIFO obligaría a la persona infartada a esperar su turno, lo cual podría ser fatal.
La Cola de Prioridad lo resuelve asignando un nivel de urgencia al entrar: no importa que la persona infartada haya llegado después, 
el sistema la reordena y la pasa directamente al frente de la fila para salvarle la vida.



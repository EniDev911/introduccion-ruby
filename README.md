## Adivina el número

```mermaid
%%{init: {"flowchart": {"htmlLabels": false}} }%%
flowchart TB
	inicio([inicio])
	-->paso1[Pedir número:\nn=gets.to_i]
	-->paso2["Generar número aleatorio:\naleatorio=rand(n)"]
	-->paso3["Intentar adivinar:\nnumero=gets.to_i"]
	-->paso4{"numero == aleatorio"}
	solicitar[Volver a intentar]
	solicitar --> paso3
	paso4 --> |Si| paso5["Mostramos por pantalla\n'¡Adivinaste, felicidades!'\n\n"]
	paso5 --> fin([Fin])
	paso4 --> |No| paso6{"numero < aleatorio"}
	paso6 --> |Si| paso7["Mostramos por pantalla\n'El número es mayor sigue intentando!'\n\n"]
	paso7 --> solicitar
	paso6 --> |No| paso8{"numero > aleatorio"}
	paso8 --> |Si| paso9["Mostramos por pantalla\n'El número es menor sigue intentando!'\n\n"]
	paso9 --> solicitar
	```

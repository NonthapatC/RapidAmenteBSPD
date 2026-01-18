BSPD Logic;
TPS1 sense = TS1
TPS1 con = TC1
TPS1 over = TO1

TPS2 sense = TS2
TPS2 con = TC2
TPS2 over = TO2

BRK1 sense = BS1
BRK1 con = BC1
BRK1 over = BO1

BRK2 sense = BS2
BRK2 con = BC2
BRK2 over = BO2

(TS1+TS2)(BS1+BS2) -> 1000ms delay -> A

[(TC1)(TC2)(TO1+TO2)’(BC1)(BC2)(BO1+BO2)’]’ -> 100ms delay -> B

Final Logic; A+B -> latch R pin

Characteristic;
Normal:
BSPD status = 0v
BSPD status led = off
Latch R1/LogiOut led = off
Relay = com connected to NO; disconnected from NC

trip:
BSPD status = 12v
BSPD status led = on
Latch R1/LogiOut = on when trip condition satisfied
Relay = com connected to NC; disconnected from NO

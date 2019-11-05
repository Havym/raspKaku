raspKaku
========

Control your KAKU with Raspberry

=======================================================================================================================

Gebruikt het nieuwe kaku protocol. Om dit te kunnen "spreken" heb je ook raspKaku nodig naast de wiringPi library:

https://github.com/Havym/raspKaku

Download deze op je pi. Een van de laatste regel in newkaku.cpp is:

NewRemoteTransmitter transmitter(address, 15, 260, 3);

parameter 15: hardcoded 433MHz data pin voor wiringPi
parameter: 260, pulse lengte
parameter 3: aantal keer signaal herhaald wordt

Verander deze parameters voor compileren indien nodig.

Compileer executable met het commando:
g++ -o newkaku newkaku.cpp -I/usr/local/include -L/usr/local/lib -lwiringPi

Nu kan je met commando ./newkaku de Action SF-501P inleren en schakelen.

Design Implementation
1. The user input will reach the circuit as three BCD numbers i.e. twelve binary
digits. The user need not ascertain the state of each device (lights or fans) with
every command; in that case, all the other digits will remain in their existing
states.
2. Our design employs the one-hot encoding as it is known to work at higher clock
rates (if needed) and allows easier identification of invalid states.
3. Our 12-bit input is broken into 4 groups of 3 inputs, each controlling one device.
Assuming the 3 BCD numbers to be A n , B n and C n , A3A2A1 controls Light 1,
A0B3B2 controls Light 2, B1B0C3 controls Fan 1 and C2C1C0 controls Fan 2.
The coding is as follows.
a. Light 1 is ON when A3A2A1 is 010 and is OFF when it’s 001.
b. Light 2 is ON when A0B3B2 is 100 and is OFF when it’s 001.
c. Fan 1 is ON when B1B0C3 is 100 and is OFF when it’s 010.
d. Fan 2 is ON when C2C1C0 is 010 and is OFF when it’s 001.
4. The Input Validation Block of the design checks if the input is a valid signal or not
and only allows further propagation of the signal if it’s valid. When invalid, the
system remains in the previous state enabled by the Memory and Output Block.
5. The circuit is able to produce the output in 6 clock cycles. We decided to prioritise
the accuracy of the circuit over the speed.
The Invalid light stays ON/blinks if the input is an invalid combination.

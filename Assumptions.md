Assumptions
1. We are assuming that the external system can convert the input given by the user
to 3 BCD numbers.
2. We are assuming all 12 inputs signals are coming at once.
3. We are assuming that the input is always 12 bit. For example, if only L1 is on, ie
input was 0100 0101 0001 (451) and we now want L1 and F1 to be on, input will
be 0100 0110 0001 (461), ie even though the user will just give the command for
F1 to be ON since L1 was already on, input for L1 won’t change and thus we will
get L1 and F1 both ON as required.
4. We are assuming that the input does not change in 5 clock cycles.
5. We are assuming that when the circuit is reset using the kill switch, the WIFI
transmitter changes the inputs to zero.
6. We are assuming only fans take considerable power and thus only their power
consumption is counted.
7. We are assuming a clock frequency of 4Hz.

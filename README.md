--- SmartPortInterfaceSharedMem Notes

xxx



(Ins and Outs relative to BBB)
Inputs:
WDATA	P8_45
P0/REQ	P8_46
P1		P8_43
P2		P8_44
P3		P8_41

Outputs:
OUTEN	P8_42	// 0=LS367 enabled, RDAT active
RDAT	P8_39
ACK		P8_40	// 1=ready to send/receive
LED		P8_27
TEST	P8_29


To Run:
source setup.sh							- to set some parameters and configure I/O pins
gcc SmartPortController -o Controller	- to compile Controller
make									- to compile PRU code and install and start
./Controller							- to start Controller

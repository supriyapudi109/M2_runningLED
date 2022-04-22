atmega328 is an 8bit AVR based microcontroller , here we implemented simple LED blinking program.
In this circuit we use atmega328, relay,buzzer and 8 LEDs. Once the hex file is burn onto the circuit and we run the circuit, we can see the LEDs glowing . 
#define F_CPU 16000000
#include <avr/io.h>
#include <util/delay.h>
int main(void)
{
	DDRB=0xFF;
	unsigned char z;
	while(1)
	{
		
		for(z=0;z<255;z++)
		{
			PORTB=z;
			_delay_ms(1000);
		}
	}
	return 0;
	}

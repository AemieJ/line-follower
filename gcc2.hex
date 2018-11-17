#include <avr/io.h>
#include <avr/sfr_defs.h>
int main(void)
{   
    DDRA=0x00 ; 
    DDRD=0xFF ; 
    char memory ; 
    while (1) 
    {
		if(!bit_is_clear(PINA,1)&& !bit_is_clear(PINA,2) && !bit_is_clear(PINA,3) && !bit_is_clear(PINA,4) && !bit_is_clear(PINA,5)){
			if (memory=='f'){  PORTD = 0b00100100 ; }
			else if (memory=='r') { PORTD= 0b00000100 ; }
			else if (memory=='l') { PORTD=0b00100000 ; } }
		else if(!bit_is_clear(PINA,3) && !bit_is_clear(PINA,2) && !bit_is_clear(PINA,1) ) {
			if(bit_is_clear(PINA,4) || bit_is_clear(PINA,5)) { //turn right 
				PORTD= 0b00000100 ;
				memory='r' ;}}
		else if(!bit_is_clear(PINA,3) && !bit_is_clear(PINA,4) && !bit_is_clear(PINA,5) ) {
			    if(bit_is_clear(PINA,1) || bit_is_clear(PINA,2)){ //turn left
					PORTD=0b00100000 ;
					memory='l' ;}}
		else if(bit_is_clear(PINA,3) && !bit_is_clear(PINA,2) && !bit_is_clear(PINA,1) ) { 
			if (bit_is_clear(PINA,4) || bit_is_clear(PINA,5) ){ //turn right 
				PORTD= 0b00000100 ;
		    	        memory='r' ;}}
		else if(bit_is_clear(PINA,3) && !bit_is_clear(PINA,4) && !bit_is_clear(PINA,5) ) {
			if(bit_is_clear(PINA,1) || bit_is_clear(PINA,2)){ //turn left
				PORTD=0b00100000 ;
			        memory='l' ;}}
	    else if(!bit_is_clear(PINA,1)&& !bit_is_clear(PINA,2) && bit_is_clear(PINA,3) && !bit_is_clear(PINA,4) && !bit_is_clear(PINA,5)){
			PORTD = 0b00100100 ;
			memory= 'f' ;}
	    else if(!bit_is_clear(PINA,1)&& bit_is_clear(PINA,2) && bit_is_clear(PINA,3) && bit_is_clear(PINA,4) && !bit_is_clear(PINA,5)){
			PORTD = 0b00100100 ;
		        memory= 'f' ;}
		else if(bit_is_clear(PINA,1)&& bit_is_clear(PINA,2) && bit_is_clear(PINA,3) && bit_is_clear(PINA,4) && bit_is_clear(PINA,5)){
			PORTD=0b00000000 ; } 
      }
}


# AVR Port selection

    In ATMEGA32A, we can give Analog input to any of eight channels of PORTA, it doesn’t matter which channel we choose as 
    all are same. We are going to choose channel 0 or PIN0 of PORTA. In ATMEGA32A, the ADC is of 10 bit resolution, so the
    controller can detect a sense a minimum change of Vref/2^10, so if the reference voltage is 5V we get a digital output
    increment for every 5/2^10 = 5mV.So for every 5mV increment in the input we will have a increment of one at digital output. 

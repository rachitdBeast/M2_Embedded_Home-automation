# setting the register of ADC based on the following terms

    1.First of all we need to enable the ADC feature in ADC.

    2. Since we  are measuring room temperature, we don’t really need values beyond hundred degrees (1000mV output of LM35).
    So we can set up maximum value or reference of ADC to 2.5V.
    
    3. The controller has a trigger conversion feature, that means ADC conversion takes place only after an 
    external trigger, since we don’t want that we need to set the registers for the ADC to run in continuous
    free running mode.

    4. For any ADC, frequency of conversion (Analog value to Digital value) and accuracy of digital output are 
    inversely proportional. So for better accuracy of digital output we have to choose lesser frequency. 
    For lesser ADC clock we are setting the presale of ADC to maximum value (128). Since we are using the 
    internal clock of 1MHZ, the clock of ADC will be (1000000/128).

    These are the only four things we need to know to getting started with ADC. All the above four features are set by two registers.
    
   ![image](https://user-images.githubusercontent.com/81420042/144307597-17cd8ec6-6860-49c6-beb9-8eaa198b7588.png)
     
     RED (ADEN): This bit has to be set for enabling the ADC feature of ATMEGA.

    BLUE(REFS1,REFS0): These two bits are used to set the reference voltage (or max input voltage we are going to give).
    Since we want to have reference voltage 2.56V, REFS0 and  REFS1 both should be set, by the table.

   ![image](https://user-images.githubusercontent.com/81420042/144307793-1c613b96-f1be-46be-b53a-788a7ba785e4.png)

    

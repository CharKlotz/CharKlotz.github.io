---
title: Resources
---

## Code: 
The following code was used to programmed to fulfill the needs of my light sensor subsystem

<details>

  <summary><strong>Microcontroller Code (Click to expand)</strong></summary>
  <pre><code class="language-c">
#include "mcc_generated_files/system/system.h"
int main(void)
{
    adc_result_t analog_in=0;
    uint8_t analog_out=0;
    uint16_t ADC_MAX=4096;
    SYSTEM_Initialize();
    ADC_Initialize();
    const float vref = 5;
    const float vin_min = 0.3;
    const float vin_max = 1.3;
    uint16_t delay_needed_ms = 0;
    uint16_t n = 0;
    
    while(1)
    {
        if(JT_Input_GetValue() == 1)
//        if (1 == 1)
        {
        ADC_ChannelSelect(ADC_CHANNEL_ANA0);
        ADC_ConversionStart();
        while (!ADC_IsConversionDone());
        analog_in=ADC_ConversionResultGet();
        
        float vin = (analog_in * vref/ADC_MAX);
        
        if (vin <= vin_min)
            analog_out = 0;
        else if (vin >= vin_max)
            analog_out = 255;
        else 
            analog_out = (((vin-vin_min) / (vin_max - vin_min)) * 255); // ratio of current voltage to the whole range * 255 to make output 0-255
        
        DAC1_SetOutput(analog_out);
        
//        analog_out=analog_in>>4;
//        DAC1_SetOutput(analog_out);
        // If Jon's system does not work:
        printf("VIn: %f\n\r",vin);
        printf("Analog out: %u\n\r",analog_out);

        
        DebugLED_Output_Toggle();
        
        if (analog_out != 0)
        {
            delay_needed_ms=(uint16_t)(1000UL - (analog_out * 950UL / 255UL));
            printf("desired ms = %u\n\r",delay_needed_ms);
            for (n = 0; n<delay_needed_ms; n++)
            {
                __delay_ms(1);
            }
        }
        else 
        {
            __delay_ms(1000);
        }
        
        // when subsystem is off according to JT's (If needed):
        }
        else
        {
            DebugLED_Output_SetHigh();
            __delay_ms(50);
            DebugLED_Output_SetLow();
            __delay_ms(200);
            DebugLED_Output_SetHigh();
            __delay_ms(50);
            DebugLED_Output_SetLow();
            __delay_ms(1000);
        }
    }    
    return 0;
}
 </code></pre>

</details>

## Resources

The code is available [*here*](main.c)

The MPLabX Project file is available [*here*](EGR304_Subsystem.zip)
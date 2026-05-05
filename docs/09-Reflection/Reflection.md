---
title: Reflection
---

## Review of Module's Sucess

The major functionality of the Human Machine Interface was completed in the sense that a person should be able to correctly interact with the machine through it, causing for different pre-defined functionalities to occur. This was achieved through the interaction of values through buttons, aswell as instant feedback through the OLED display, aswell as the ability to pass through other teammates values. 

Unfortunately full functionality of our rover could not be confirmed as not everyone had their boards in a workable state to test everything by the end. Some messaging was achieved, however, at least through mine and another persons PCB, proving its functionality. 

Overall, module requirements should have been fully met, but there was no way of completely confirming.

## Microcontroller/Module Startup Tip

I definetely tried to do too much at once when populating the pcb. I definetely recommend placing components 1 by 1, checking continuity, and verifying functionality of individual components once down however possible. This caused a major headache with the microcontroller, where when you dont know if its the power input thats wrong, or the boot logic, or the switch connections, it could get difficult to debug fast.

Trying to do too much with data received and sent through TX and RX at once could cause everything to break. Verify you receive at all, then go step by step to process it into what you want.

## Lessons Learned

1. Read datasheets carefully, look for unique pin details or restrictions, recommended circuits/logic.
2. Keep TX and RX communication very very simple to start off with.
3. Sort out the team API before things get too far. 
4. This stuff takes longer than you think. Don't give yourself hours to do things.
5. Work up with your code slowly, find what works, and build off of it. 
6. Check EVERYTHING
7. Debug more with breadboard circuits.
8. More testing points and LEDS
9. Order extra parts
10. Update your github as you go

## Recommendations for Future Students

1. Build your PCB early, give yourself time to find your own mistakes. Get it looked at by the professor in detail, then submit.
2. Spend extra time with labs that will have to do with the functionality of your subsystem.
3. When things aren't working, focus on the small victories and build off of them. 
# blink03
4 lines added into blink02, LED pin level HIGH/LOW period could be changed interactively as well.


1. 2 function setPeriodHIGH() and setPeriodLOW() are defined as follows:

        void setPeriodHIGH() { periodHIGH=F.dPop(); }       // ##### 2.1. define the function setPeriodHIGH
        void setPeriodLOW()  { periodLOW =F.dPop(); }       // ##### 2.2. define the function setPeriodLOW


2. in setup(), 2 virtual machine new words are created as follows:

          F.newPrimitive( "setPeriodHIGH", setPeriodHIGH ); // ##### 4.1. add new primitive word setPeriodHIGH in F
          F.newPrimitive( "setPeriodLOW",  setPeriodLOW  ); // ##### 4.2. add new primitive word setPeriodLOW  in F

3. Once this code is running, via IDE consle input box, delay period of HIGH or LOW could be set at any time.


4. For example, sending "50 setPeriodHIGH 450 setPeriodLOW" to virtual machine, via IDE consle input, will
   change the way LED blinks as short HIGH.
   
   
5. Even more, 2 new words, namely shortHIGH and longHIGH , could be created in IDE input box as follows:

                : shortHIGH 50 setPeriodHIGH 450 setPeriodLOW ;
                : longHIGH 450 setPeriodHIGH 50 setPeriodLOW ;


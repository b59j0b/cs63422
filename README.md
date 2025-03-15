java c
Department of   Bioengineering   
MEng    Engineering Courses
Arduino   1st   Year Task sheet
Summer   Term, 2021
Syllabus:
•          The   uses   of   Development   kits   and   role   in   product   development.      Standard   tools   available   for
development work, role of   Open   Source tools.    The marketplace of   development system / tools.
•          Alternative   technologies   to   embedded   microprocessor   based, and   relative   choices.
•          Programming   an   embedded   processor   with   a   high-level   language   (C):       A   range   of   commands,   program control, developing a clear   style.
•          Basic   concepts   of data   flow   in   an   embedded   system:   Analogue   to   digital   conversion,   Digital   to   Analogue conversion, sensors and transducer.
Learning Outcomes:
At   the   end   of   this   course,   participants   will   be   able   to:
•          Code a   Sketch   in Arduino   code,   download   it   into   a target board   and   test   it runs
•            Describe   the   typical   uses   ofan   Arduino
•          Place    the    Arduino    in   the   marketplace    of   available   development   system,   with   its   relative   advantages and disadvantages against other possible solutions
AssessmentThis activity forms part of   Design and Professional Practise. The intention is you keep   a portfolio and   demonstrate that   you can setup a commercial development environment and   use it to   write and modify   code, and then download it to given hardware.
Introduction and Overview
You   should   have   now   received   a   kit   of   parts:
•            Arduino (Nano or UNO)
•            Solderless breadboard, if   needed, with wires
•            LED, Resistor, Buzzer (possibly not)All students with a PC should have downloaded Arduino version   1.8.12.      There is a link from   the imperial software hub.    Students with an apple   device   should have   downloaded the   latest   Arduino   IDE   for Mac.   For this task, please   download   the   IDE   for   the   desktop   –   do   not   run   from the web-based web app.If   you have a Nano, supplied by the college it will have the CH340 USB chip.    Your PC may   not   have   the   driver   for   this   device. How   to   Install   CH340 Drivers   -   learn.sparkfun.com         has   a   lot of   good   advice   on   this   topic, and   many   others   to   do   with   Arduino.You may wish to   come back   to this   task   -   or   take   this   further   (perhaps   for   a   project?).      The   activities   are   mainly   of   a   practical   nature.   There   will   be   technician   and   GTA   support   at   prearranged   times   – if   you   are   unclear   of   anything   please   ask   – there   are   no   silly   questions!
Introduction:As   digital   logic   has   progressed   (Moore’s   law   -   if unaware   of -   google   it)   the   role   of small   computers has evolved.   The Television and computing have, to an extent, converged.    There   are   increasingly   very   small   computers   doing   trivial   tasks   -   in   a   car   the   door   may   contain   a   small computer that reads the up /down buttons and operates the motor accordingly.   This has   led to a very, very, big market for “micro-controllers” – a whole small   computer   on   a   chip
Naming   Convention:
“Microprocessor” – the   CPU   –   “central   processing   unit”   of   a   computer   -   this   might   be   very   large   –   e.g. Pentium processor clocking at 3GHz with over   1000 pins, or very   small, clocking   at,   say,   1Mhz.
“Micro-Controller” - A single chip computer.    Typically contains the CPU and   some memory (non – volatile for the program, volatile for data) and input/ output circuitry etc.    Very small, cheap- pennies.“SoC”   –   System   on   a   chip.      Some   markets   are   so   large   that   it   is   worthwhile   to   deliver   a   dedicated   integrated circuit   just for that functionality.    They typically contain one or more microcontrollers, and   some   dedicated   logic   circuitry – perhaps   designed   in   a program   like   Quartus   II.          Examples   include   televisions, consumer electronics, games, medical devices.“Open   Source” -   Some   software is released “free” to use.          Typically, the company will aim to   make profit   from   added   services,   for   example   technical   support.      There   is   a   lot   more   to   this   –   “free”   is   a   complex   term.“Development   board”: To   sell   a   microprocessor   chip   the   chipmaker   often   designs   an   example   system   or “development board”.       This   saves the   system designer   a   lot   of   the   design   work.   Buying   the   chips   allows   you   to   copy   elements   of   the   design   (care   needed   for   commercial   products!).
What   is   an   “Arduino”Arduino is an “open source” hardware “platform”   .      It is a small printed circuit board with components   on.      It   is   also   a   software program running   on   a   PC   (or Mac).       The   software   is   an   “IDE”   -   Integrated   Design   Environment.    If   you   want   the   code   to   read   a   temperature   sensor,   or   the   code   to   play   a   tune   –   somebody else has already written   it and published it (better to give than receive!).   The circuit design   for the hardware   is   openly published. The code   for   the   IDE   is   published.   “Open   Source”   –   good   and   bad.    You   may   prefer   the   comfort   of   being   a   customer   - with   commercial   liabilities.
See Appendix A   for competitors   for Arduino –   The   Arduino   sits   in   a   market-place   worth billions   of dollars   of   microcontrollers   and   development   kits   for   microcontrollers.
Ifa   “Compiler   fell   on   your   toe- would   it   hurt?”Arduino calls programs “Sketches”   .    The Arduino IDE include a “compiler”   .    A complier takes a text   file   of commands   in the   chosen high-level   language   (in this   case   C)   and produces machine   code,   1s   and   0s   of valid   instruction   for   the   chosen   micro-processer.   So,   a   compiler   is   a   software   tool,   like   Microsoft Office, or Matlab are. Also had an upload function – writing to the hardware.

TASK1:    introduction: Writing your first “Sketch” (program).
BLINK!

a.          Everything   between      /*   …   .    */          is   ignored      -   it   isjust   a   comment   for   us   humans.
b.          Everything   on   a   line   after   // is   ignored   -just   a   comment
c.          Every   command   inside   {      …   .   }    becomes   like   one   statement   together
d.          Every “sketch” has a setup part (which   is   only   done once)   and   a   loop part   which   is   done repeatedly.
e.          Every   command   is   separated by   ;
f.          “Compiling” turns   this   text   file   into   an   executable program   for the Arduino   (the buttons   “compile”
and   “upload” are   in   menu   bar      .         (Hover   on   them!).
g.          “Uploading” sends the executable to the Arduino –which   stores it   permanently   and runs   it.
h.          The   “IDE” helpfully   colour   codes- grey   for   comments   etc.
TRY IT!
(Blink is already typed in for you – if   you   start IDE program   open
file/examples/basic/blink)
1.       (Will need   to   go   into   tools   menu   and   select   which   device   you   have-   i.e. Nano   or   UNO)   and   possibly   which   USB   port   your   device   is   on   –   typically   the   highest   value   e.g.   COM9.       See   appendix D for more help details.
2.       After   compiling   and   uploading   – prove   to   yourself   it   is   stored   in   the   Arduino.      Unplug   it   and plug back in again- without downloading again or even opening Arduino IDE- is it still there?   Still blinking?
You have written, compiled, downloaded and test a   simple program!
3.       Try replacing LED_BUILTIN with   13, does   it   still work?
4.       Is   “digitalWrite”   case   sensitive?   (try   it)
5.       Try varying the relative delays for the time   on   and   the   time   off.      What units   are the   argument   of   delay   in?
6.       If you   have   one,   connect   the   buzzer   between   pin    13   and   ground   (find   it   on   Arduino   –   it   is   labelled).       “Middle C” is 262Hz   (i.e. 262   cycles per   second).      Can   you   make   a   noise   / play   a   tune? /   is resolution   of delay   function   fine   enough?             Is there   a   similar   function with   a   finer   resolution   –   e.g. microseconds?   (Google?)    (If   you   do   not   have   a   buzzer-   an   old   headphones or a small speaker from an old radio would   do   instead –   else   omit   this part).
TASK2: Developing “blink” program into Pulse Width modulation – simple exampleWe have   seen we used a “function” called   “delay”.         A   function   is   a number   of   lines   of   code   we can   call   up   as   one-   like   a   program   within   a   program.      Typically,   it   has   one   or   more   argument   inputs, and may return a value.
There are a large number of   pre-written functions (such   as   delay) – or we   can write   our   own.The output pins ofthe Arduino are wholly digital – they can output a 0 (=0V) or   a   1   (or   “high”) =   5V. Often we want not   just an on or ff= but a variable (e.g. the speed of   a motor- the energy into  代 写Arduino 1st Year Task sheet Summer Term, 2021Matlab
代做程序编程语言 a   heater   etc.). Arduino   copes   with   that   by   use   of“Pulse   Width   Modulation”.
Tasks
Rewrite   “blink”   so that the output is high   for   10%   of   the   time   and   low   for   90%   of   the   time   (and   the frequency >50Hz). Repeat for 90% high /   10% low. Note brightness   of   led.
We   have   just   done   “pulse   width   modulation” – the   signal   –or   value   –   modulations   (controls)   the width   of   the   pulse.We want to use the PWM   process   a   lot.      The   chip   inside   the   Arduino   has   some   circuitry   to   do   it   for us. The IDE gives us a   function   to   call   it   up   (AnalogWrite).   Open   the program   “Fade”   which   is in the Files\examples\Basic menu.
Notice The function “AnalogWrite” has two arguments. What are they?
a.       Investigate   “tone”   function.      Write   a   sketch   to   play   a   tune   of   your   choosing.   (If   have   buzzer or   speaker)
b.       Investigate “libraries” and the   “include”   compiler   directive.
Task   3: Inputs: Use   of   “sensors”
We saw in the last task, while the Arduino has no analogue outputs – it has pseudo ones by the use of   PWM. To process analogue values the Arduino has six analogue inputs. (Named A0   to A5).
The analogue inputs, by default, return a number between 0 and   1023 – representing between   0V   and   5V
Tasks:
1.       Take a wire from pin marked A0   to pin marked 3.3V       Run AnalogSerialRead   (in the   examples directory).   Run   the serial   monitor (in   tools).   What   value is   returned for 3.3V.   Move the wire from 3.3V to 5V – should now see   1023- What is   (3.3/   5)*1023? Now   move to GND, what do you see?    Leave it   dangling   - what   do you   see?
2.      Experiment   with   serial   plotter   (if on   your   version   Arduino   IDE   –   not   on   all).          It   is   almost like your own oscilloscope – admittedly at very low   frequencies!We   can   think   of almost   any   microprocessor based   system   as being   some   real process   (“the   real world”) which we measure – with a sensor and an ADC, some processing power, a DAC   and then actuator / transducer.       We measure the real world, think about it, and do something   about it.       (A classic example is a heating system- the heat output   is inversely proportional to the temperature difference between the actual measured temp and the “set point”).Figure 4
3.      For the following systems – State which is input,   output, and what   the process   going   on   is?
a.          A Television
b.         A cash machine
c.         A hospital ultrasound   scanner
d.         A digital   stethoscope
e.         A TENS unit
Other ideas: (All optional   -Summer fun!)
1.       Use   the   circuit   in   appendix   A   to   control   a   motor   or   a   light   bulb   (will   need   to   source   a   npn   transistor and a dc motor – perhaps from a   toy?)
2.       If   you have potentiometer available connect its ends between 3.3V and GND.    Then the wiper   will be a variable voltage.    Read it (using analogRead)   and   change value   of   tone.         (Careful – the input is   10bit (0->1023) the output is   8 bit   (0->255).
3.         Investigate “map” function.
4.         Go back on a circuit you made elsewhere   –   e.g.   stethoscope   or   digital   logic   tasks.      See   if   can   do it with an Arduino and in   software   - which is better?
5.       Install a   frequency measuring   app   on   a phone   -   and   look   at   spectrum   of   the   output   of   tone.
6.         Get a BLE (Bluetooth Low Energy module) and   pair it with   a mobile   device.
7.       Use “Tone” at   very low frequency” and feedback   toA0 (Analog in).   Watch   with Serial   plotter.   Investigate code for “low pass frequency filtering”, effect   on wave   form.      (Actually,   a   simple   low   pass   filter   can   be   a   “running   average”   -e.g.   the   average   of   the   last   3   samples-   can   implement with 3 variables – or better an “array” and a “pointer”).
Appendix A: Competitors to Arduino:Using the Arduino is   one way to develop a digital system. If   the system is to be in relatively high cost,   small   numbers   it   is   possible   that   an   Arduino   could   be   in   the   final   product   sold.      Alternatively,   the   circuitry from   theArduino can   be copied (ithas a   main   microcontroller   from   Atmel), and amalgamated   with    any    add-on    ICs    to    make    a    final    circuit.    In    that    case,    we    are    using    the    Arduino    only    for   development purposes-   it   is   our   “development platform”   .   Most micro   controller IC makers   have   for   sale development platforms to facilitate designing in their IC into your products.    Suppliers like NXP,   Freescale,   ST   all   sell   ICs   based   upon   the   ARM   micro-processor   and   have   a   range   of development   platform.   Texas   Instruments   (ti)   have   their   “Launchpad”   range   which   are   similar   to   Arduino   –   but   higher cost, greater functionality, and a little less   accessible   to   get   started.
Raspberry Pi:This   is based upon   a   Broadcom ARM processor   (the   type   that   might   be   found   in   a   tablet).   It   is   low   cost. It is nearer a PC – for example it has   a   socket to plug   a   monitor   in,   and   a USB   host   socket.      It   is   aimed at the hobbyist market, similar to Arduino – but higher cost, higher functionality.      It is perhaps   more accessible – it run lynux and presents similar to a PC type desktop.       Coding   tools for a range of   users have been developed – including children.
PICPrior   to   Arduino   the   major   IC   for   small   simple   /   hobbyist   embedded   systems   were   the   PIC   family.   Very low cost development board are available – and so much functionality is on the chip it takes very   little   extras to make   a   system.   Often PICs were programmed   in   assembler   language   –which   is   more   like the machine   code – but   C   compiler   are   available.      The   PIC   family has   a   wide   range-   from   very   simple   in   8   pin   packages,   to   complex   ones   with   a   lot   of   input/   output   including   USB,   complex   processors, and many extra blocks.
FPGA:“Field   Programmable   Gate   Arrays”   are   ICs   with   arrays   of   NAND   gates   and   flip   /   flops   /timers   etc.   They come “uncommitted”.      There is programmable interconnection between the gate and timers etc.   We   can   program   in   combinatorial   and   sequential   logic   functions   into   them,   using   a   development   system such as Quartus II.       (Quartus is the   compiler, which   takes   the   designed   logic   relationship   and   translates   it   into   which   fuses   to blow   or   leave   intact to   interconnect to   give   that   functionality).   One   can buy low cost development boards.It is not unusual for a new   design   –for   example   in   a printer-   to   go   into   production   with   the   design   on   an FPGA and after many   10s of   thousands sold for the   design   to be   moved   to   a   dedicate   SoC   (system   on   chip).
PC:For complex   systems it is not unusual to use a   PC   board   in   an   embedded   system.      For   example   many   tills and medical devices are actually PCs – in a smaller size called PC104.      This reduces development   costs- but increases unit costs (but many start-ups are   short on   capital – but intend   a high   margin).
Appendix B: Controlling Real things (optional)The   Arduino   has outputspins   that are set to   be 0V or 5V.       They are   not designed   to   provide significant   energy.          (If we   present   a   load   of   1k   Ohms   to   ground   then   5mA   will   flow   out-   good   engineering   suggests   do   not   exceed   this   by   much-   but   pins   are   actually   rated   a   little   higher).          We    can   use    a   transistor as a switch, to “buffer” the pins.    Below is a BJT (bipolar   junction transistor) version of   the circuit.
1.       Build   this   circuit   on   breadboard   and   modify   your   code   so   that   the   motor   toggles   every   2s   between   two   distinct   speeds.   (May   need   to   use   a   different   generic   npn   BJT).   The   lab   has   numerous –look at marking, i.e. the number and find its “pinout”   online.
2.       Research “flywheel diode” and thus   explain its use   in   the   circuit below.

Appendix C: Problems with Wearables and Arduino /   BLE
1.       Many devices   which are intended to   be “wearable” come across   body fluids/ sweat etc -liquids   and electronics do not mix well.
2.       There    are    mechanical   issues   with   making   a   rigid   PCB   and   battery   conform   to   a   moving   biological   surface.             There   are   particular   problems   with    any   wire   connections   /   typically   soldered.    Conductive thread is sometimes used — perhaps better to have no wires?
3.       Flexible PCBs are possible — maybe a   more   suitable   technique   for   a wearable?
4.       The   Arduino   is   not   optimised   for   low   power   (in   a   wearable   power   consumption   is   critical)   other very low power devices optimised for battery usage are available
5.       If   Arduino is used —   it is probably best to use one with BLE   (Bluetooth Low   Energy) built in.



         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com

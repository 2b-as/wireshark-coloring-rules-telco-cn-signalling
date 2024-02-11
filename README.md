# Wireshark Coloring Rules for SIGTRAN/Diameter/GTP Signalling

Make it easier to see what is going on with SIGTRAN/Diameter/GTP
signalling in Wireshark by colorizing the packets according to their
type.

To install the rules, create a new profile in Wireshark and then
either copy the `colorfilters` file into the new directory of the
profile or, if a `colorfilters` file already exists for the in that
diretory, concatenate the two files.

These rules have been tested mostly with interconnect traffic between
networks. For other traffic (especially Diameter and GTP) your mileage
might vary.

This is how the packets will be colorized:

|Message Type|Color|
|------------|-----|
|MAP/CAMEL invoke / ... in a TCAP Continue|![](https://placehold.co/100x15/bafffd/bafffd.png) ![](https://placehold.co/100x15/b8ccfe/b8ccfe.png)|
|MAP/CAMEL returnResult(Not)Last / ... in a TCAP Continue|![](https://placehold.co/100x15/beffb4/beffb4.png) ![](https://placehold.co/100x15/83ffb4/83ffb4.png)|
|MAP/CAMEL returnError or reject / ... in a TCAP Continue|![](https://placehold.co/100x15/ffaab0/ffaab0.png) ![](https://placehold.co/100x15/ffa980/ffa980.png)|
|Empty TCAP Begin|![](https://placehold.co/100x15/2cb1ff/2cb1ff.png)|
|Empty TCAP Continue or End|![](https://placehold.co/100x15/7bef81/7bef81.png)|
|TCAP Abort|![](https://placehold.co/100x15/ea514e/ea514e.png)|
|SCCP (X)UDTS|![](https://placehold.co/100x15/800700/800700.png)|
|Diameter request|![](https://placehold.co/100x15/bafffd/bafffd.png)|
|Diameter answer successful (2001)|![](https://placehold.co/100x15/beffb4/beffb4.png)|
|Diameter answer with application error|![](https://placehold.co/100x15/ffaab0/ffaab0.png)|
|Diameter answer with protocol error|![](https://placehold.co/100x15/ea514e/ea514e.png)|
|GTP request|![](https://placehold.co/100x15/bafffd/bafffd.png)|
|GTP accepted|![](https://placehold.co/100x15/beffb4/beffb4.png)|
|GTP error|![](https://placehold.co/100x15/ffaab0/ffaab0.png)|

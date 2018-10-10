# netlogo-osc
Netlogo extension that allows to send OSC messages from it to other software (for more info see [complete documentation](https://quod.lib.umich.edu/cgi/p/pod/dod-idx/osc-netlogo-a-tool-for-exploring-the-sonification-of-complex.pdf?c=icmc;idno=bbp2372.2012.069;format=pdf) by Rodrigo Cádiz and Marco Colasso)
The OSC-NETLOGO Extension for NetLogo adds primitives to NetLogo that allow users to send data from NetLogo models via OSC to third party applications. Turtles, Breeds, Links, Patches and any other variables from a NetLogo patch can be routed to a compatible external hardware or software, via Ethernet.

## Installation 
It can be installed in two different ways:

• Put the osc folder into the Extensions folder in the
same location where the NetLogo application is installed.

• Put the osc folder into the current model folder.

After installing the OSC extension, in order to use it,
it is mandatory to add the following line to the top of the
procedures tab: extensions [osc]

# netlogo-osc
OSC is a Netlogo extension that allows to send OSC messages from it to other software (such as Puredata, Wekinator, among others). This is an update of the [original version](https://quod.lib.umich.edu/cgi/p/pod/dod-idx/osc-netlogo-a-tool-for-exploring-the-sonification-of-complex.pdf?c=icmc;idno=bbp2372.2012.069;format=pdf) made by Rodrigo Cádiz and Marco Colasso, which is compatible with the last version of Netlogo (6.x).  
The OSC-NETLOGO Extension for NetLogo adds primitives to NetLogo that allow users to send data from NetLogo models via OSC to third party applications. Turtles, Breeds, Links, Patches and any other variables from a NetLogo patch can be routed to a compatible external hardware or software, via Ethernet.

## Installation 
It can be installed in two different ways:

• Put the osc folder into the Extensions folder in the same location where the NetLogo application is installed.

• Put the osc folder into the current model folder.

Then, in order to use it, it is mandatory to add the following line to the top of theprocedures tab: extensions [osc]

## Primitives 
(taken from the original [release documentation](https://quod.lib.umich.edu/cgi/p/pod/dod-idx/osc-netlogo-a-tool-for-exploring-the-sonification-of-complex.pdf?c=icmc;idno=bbp2372.2012.069;format=pdf))

### osc:port-out
This primitive should be used in the setup of the model. The user can set the IP (String) and port number (integer)of the receiving host, such as:
```
osc:port-out "169.254.183.129 " 10000
````

If port-out is not defined, the extension will use the default parameters, ip: localHost and port: 57110.

### osc:send-agents 
This primitive receives as input a string with the name of the OSC tag, followed by the name of an agentset of the model, and names of default or defined variables for this agentset, and sends them out. The syntax for this primitive is:
```
osc:send-agents "tagName" agentsetName var1 var2 var3 ...
```
Examples:
```
osc:send-agents "myTurtles" turtles "xcor" "size"
osc:send-agents "breeds" cars "XCOR" "age"
osc:send-agents "links" blue-links "weight"
osc:send-agents "patches" patch 2 2 "pcolor" "pxcor"
```
### osc:send-variables
This primitive receives as input the name of any variable of the model and sends it out. Example:
```
osc:send-variables "decays" decays
```


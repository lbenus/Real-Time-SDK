Transport API Consumer Training Application Description
Module 1a: Establish network communication 

--------
Summary:
--------

In this module, the application initializes the Transport API and 
connects the client. An OMM consumer application can establish a 
connection to other OMM Interactive Provider applications, including 
 LSEG Real-Time Distribution Systems, Data Feed Direct, 
and LSEG Real-Time.

Detailed Descriptions:
The first step of any Transport API consumer application is to establish a 
network connection with its peer component (i.e., another application 
with which to interact). An OMM consumer typically creates an outbound 
connection to the well-known hostname and port of a server (Interactive 
Provider or ADS). The consumer uses the rsslConnect() function to initiate 
the connection and then uses the rsslInitChannel() function to complete 
channel initialization.

-----------------
Application Name:
-----------------

ConsMod1a

------------------
Setup Environment:
------------------

The RDMFieldDictionary and enumtype.def files located in the etc directory
can be located in the directory of execution. If the dictionary files
cannot be found, they are requested from the provider.

-------------------
Command line usage:
-------------------  

ConsMod1a
(runs with a default set of parameters (-h localhost -p 14002 -i ""))

or

ConsMod1a [-h <SrvrHostname>] [-p <SrvrPortNo>] [-i <InterfaceName>]
			
- ConsMod1a -? displays command line options.  

- Pressing the CTRL+C buttons terminates the program.  

-----------------
Compiling Source:
-----------------

The included makefile is set up to run from the file
locations as presented through the distribution package.
It is set up for building on the Transport API supported 
Linux platforms using the supported compilers.

The COMPILE_BITS value in the makefile is used to control
whether 32 or 64 bit version of the application is built.  
If a 64 bit application build is desired, COMPILE_BITS should
be set to 64 (which is the default setting).  If 32 bit 
application build is desired, COMPILE_BITS should be set
to 32.  

The LINKTYPE value in the makefile is used to control
whether the application is built using Transport API static or 
shared libraries. The default build uses Transport API static 
libraries. To use Transport API shared libraries, 
set LINKTYPE=Shared.

To compile, run the gmake command.

Gmake can be obtained at http://www.gnu.org/software/make/

For windows platform, using Visual Studio, open one of the included vcxproj project
files and build.

----------------
Example Content:
----------------

Included for this application are:

- Source files.

- This document.

--------------------
Detailed Description
--------------------

Consumer_Training.c - The main file for the Transport API Consumer Training application.


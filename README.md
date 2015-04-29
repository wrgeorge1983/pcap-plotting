# pcap-plotting
IPython notebooks, modules for pcap analysis, plotting

##Quick instruction for using nbviewer to view these
Derived from [watsonic's answer on stackoverflow](http://stackoverflow.com/questions/19744286/hosting-ipython-notebooks-on-github)  
> The trick is to head to your file's page on github and then click on the "Raw" button:  
> Then copy the url (minus the protocol string "http://"), and prepend it with "http://nbviewer.ipython.org/urls/"  
> So for example, for the IPython notebook:  
> https://github.com/wrgeorge1983/pcap-plotting/blob/master/pcap.ipynb  
> Click on "Raw" to get the URL:  
> https://raw.githubusercontent.com/wrgeorge1983/pcap-plotting/master/pcap.ipynb  
> Form the URL:  
> http://nbviewer.ipython.org/urls/raw.githubusercontent.com/wrgeorge1983/pcap-plotting/master/pcap.ipynb  
> voila!  



## pcap.ipynb
Initially derived from [Dirk Loss' example here](dirk-loss.de/ipython-pandas-2013-05/pcap2.ipynb)
* Early example, need to merge example from other workstation.
* [nbviewer link](http://nbviewer.ipython.org/urls/raw.githubusercontent.com/wrgeorge1983/pcap-plotting/master/pcap.ipynb)  


## pandas-testing.ipynb
Tests to determine best method of dataframe manipulation to what we want.
* 	[nbviewer link](http://nbviewer.ipython.org/urls/raw.githubusercontent.com/wrgeorge1983/pcap-plotting/master/pandas-testing.ipynb)  

## relevant projects
I can't decide whether or not these projects are relevant or not.  Best to document them and figure it out later, rather than just idly thinking about it until I forget where they are.
*	[Wireshark/TShark](https://www.wireshark.org/docs/man-pages/tshark.html)
	* Getting some better statistical analysis and prettier graphs than these provide was a large source of initial inspiration for project.
	* 'Best-in-class' packet dissectors. TShark will give you any fields you can isolate with Wireshark display filters.  *Desirable*
*	[TRPR](http://downloads.pf.itd.nrl.navy.mil/docs/proteantools/trpr.html)
	* Another large source of inspiration.  C/C++ project.  
*	[pypcap](https://code.google.com/p/pypcap/)
	* Looks like it interfaces with libpcap directly.  Probably better than piping from tcpdump?
	* There's more than a few forks of this floating around, so if this is at all where we go, worth figuring out which one to clone
	* Actually looks like [it's on pypi](https://pypi.python.org/pypi/pypcap)
	* Saner for implementing realtime plotting/analysis
*	[dpkt](https://pypi.python.org/pypi/dpkt)
	* > fast, simple packet creation / parsing, with definitions for the basic TCP/IP protocols
	* lighter weight alternative to TShark packet dissection?
	* Saner for implementing realtime plotting/analysis 
	* pypi page actually points [here](https://code.google.com/p/dpkt/)
*	[pcap-parser](https://pypi.python.org/pypi/pcap-parser)
	* Almost certainly not something we want to build off of, but might be worth a look at how they handle things for inspiration
*	[pcapy](https://pypi.python.org/pypi/pcapy)
	* looks like an alternative to pypcap
*	[scapy](http://www.secdev.org/projects/scapy/)
	* Scapy is a powerful interactive packet manipulation program. It is able to forge or decode packets of a wide number of protocols, send them on the wire, capture them, match requests and replies, and much more.
		* 'De facto standard' for command-line packet manipulation
		* That's a lot of features, and it may be difficult to encapsulate it in a sensible manner

	

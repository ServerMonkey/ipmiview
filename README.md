# Supermicro IPMIView Wrapper
A wrapper for the Supermicro IPMIView toolset.

Run "ipmiview" to start the graphical server manager.  
Run "ikvm" from terminal to use the wrapper script for iKVM.jar .  
The tool "supermicro-auto-browse", let's you automatically login to Supermicros IPMI webfrontend.

Uses Supermicros bundled JRE for best compatibility.

Tested on Debian 11

## USAGE

	ikvm -h
	supermicro-auto-browse -h
	ipmiview -h

## BUILD
Due to IPMIview being proprietary software and Supermicro not providing historical versions, it becomes challenging to release a bundled stable version.

Consequently, building the .deb package becomes a necessity.

To simplify this process, the *'make-deb-package'* script automates the download of the latest version.

If for some reason it is not possible to download the necessary file from
supermicro.com, you can provide the IPMIview package yourself.
Your file has probably a name like this:   *'IPMIView\_x.xx.x\_build.xxxxxx\_bundleJRE\_Linux\_x64.tar.gz'*  
Put this file in this folder and rename it to:  
*'ipmiview.tgz'* . Then run *'make-deb-package'*.

When building this package you automatically agree to Supermicros End User License Agreement. Which can be found here:  
https://www.supermicro.com/en/solutions/management-software/ipmi-utilities  
and probably here:  
https://www.supermicro.com/about/policies/disclaimer.cfm

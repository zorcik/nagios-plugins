Prerequisite for MegaCli installation

==========================
The MegaRAID �  MegaCli application depends on few standard libraries. 
Please ensure that these libraries are present in the system before installing MegaCli rpm. 
MegaCli will not function without these libraries.

For your convenience, above libraries are available in the rpm <Lib_Utils-1.xx-xx.noarch.rpm> and <Lib_Utils2-1.xx-xx.noarch.rpm>.
<Lib_Utils-1.xx-xx.noarch.rpm> and <Lib_Utils2-1.xx-xx.noarch.rpm> are packaged in the MegaCli zip file.
To install the <Lib_Utils-1.xx-xx.noarch.rpm> and <Lib_Utils2-1.xx-xx.noarch.rpm>, please follow below steps.

1) unzip the MegaCli package .
2) To install the Lib_Utils RPM, run the command "rpm -ivh <Lib_Utils-1.xx-xx.noarch.rpm>"
3) To install the Lib_Utils2 RPM, run the command "rpm -ivh <Lib_Utils2-1.xx-xx.noarch.rpm>"
4) To install the MegaCli RPM, run the comand "rpm -ivh <MegaCli-x.xx-x.i386.rpm>"
5) To upgrade the MegaCli RPM, run the comand "rpm -Uvh <MegaCli-x.xx-x.i386.rpm>"

Please follow the steps to use 32 bit MegaCLI to communicate with VMWARE Cosless machine.

Open the file cliVmWare.conf which is present in the same directory as MegaCLI. 
Enter the IP address of VMWARE Cosless machine in the parameter location. 
Enter the Administrator user name and password of VMWARE Cosless machine. 

With above parameters set correctly, MegaCLI will start executing MegaCLI command on the remote VMWARE Cosless machine.


Notes:
1. If older version of the libutil or libutil2 rpm (i.e. <Lib_Utils-1.xx-xx.noarch.rpm> or <Lib_Utils2-1.xx-xx.noarch.rpm>) is installed on the system, 
    please uninstall the older version of the RPM using the command "rpm -e <Lib_Utils-1.xx-xx>" or  "rpm -e <Lib_Utils2-1.xx-xx>"
    and then install the latest libutil rpm <Lib_Utils-1.xx-xx.noarch.rpm> or <Lib_Utils-1.xx-xx> packaged in this zip file.

2. If older version of the libutil rpm <Lib_Utils-1.xx-xx.noarch.rpm> is installed on the system, 
    To perform upgrade from previous version to latest version run the command 
    "rpm -Uvh --nopostun <Lib_Utils-1.xx-xx.rpm> ". 
	
3. If older version of the libutil rpm <Lib_Utils2-1.xx-xx.noarch.rpm> is installed on the system, 
    To perform upgrade from previous version to latest version run the command 
    "rpm -Uvh --nopostun <Lib_Utils2-1.xx-xx.rpm> ". 	

Example: 
   If "Lib_Utils-1.00-06.noarch.rpm" is installed on the target system to to perform upgrade to latest RPM
   "Lib_Utils-1.00-07.noarch.rpm" run the command  "rpm -Uvh --nopostun Lib_Utils-1.00-07.noarch.rpm".

4. On RHEL-3 (X64) and SLES-9 (X64), MegaCli requires libstdc++.so.6. It is assumed that these standard libraries are present in the system.
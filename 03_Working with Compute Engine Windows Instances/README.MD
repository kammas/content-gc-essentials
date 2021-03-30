# Working with Compute Engine Windows Instances
Install Windows VM, Connect via RDP, Setup IIS, CHeck IIS
Compute Engine --> VM Instances -> Create -> New VM -> Windows server 2019 with Desktop -> RDP set Password -> PoweShell (Run as administrator)- on the remote VM

```
import-module servermanager

Set up the web server:

add-windowsfeature web-server -includeallsubfeature

Create the index.html page:

echo '&lt;!doctype html>&lt;html>&lt;body>&lt;h1>Greetings from Linux Academy!&lt;/h1>&lt;/body>&lt;/html>' > C:\inetpub\wwwroot\index.html
```
Click on External IP -> Browser shows page (due to enabling Http)
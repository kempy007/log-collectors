# log-collectors

Download https://download.sysinternals.com/files/Sysmon.zip and extract contents, Open CLI as admin then cd to extract folder.

#64bit os
```
Sysmon64.exe –i –n 
```

#32bit os
```
Sysmon.exe –i –n 
```

Download https://nxlog.co/system/files/products/files/348/nxlog-ce-2.10.2102.msi and install.
Copy attached conf file to C:\Program Files (x86)\nxlog\conf\
Open services.msc and start the nxlog service.

Check "C:\Program Files (x86)\nxlog\data\nxlog.log" for any errors.

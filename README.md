
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

# RHEL ElasticSearch + Kibana

alternate versions at https://www.java.com/en/download/manual.jsp
```
wget http://javadl.oracle.com/webapps/download/AutoDL?BundleId=233161_512cd62ec5174c3487ac17c61aaa89e8 -O java64.rpm
rpm -i java64.rpm
```
```
wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-6.2.4.rpm
rpm -i elasticsearch-6.2.4.rpm
systemctl enable elasticsearch.service
```
set the bind IP address
```
nano /etc/elasticsearch/elasticsearch.yml
systemctl start elasticsearch.service
```
```
wget https://artifacts.elastic.co/downloads/kibana/kibana-6.2.4-x86_64.rpm
rpm -i kibana-6.2.4-x86_64.rpm
```
Set the ElasticSearch URL 
```
nano /etc/kibana/kibana.yml
systemctl start kibana
```

restrict access to the ElasticSearch Port(9200), and use ssh tunnel to get to Kibana port http://127.0.0.1:5601

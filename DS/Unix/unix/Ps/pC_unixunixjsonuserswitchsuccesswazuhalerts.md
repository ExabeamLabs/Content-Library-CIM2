#### Parser Content
```Java
{
Name = "unix-unix-json-user-switch-success-wazuhalerts"
Product = "Unix"
Vendor = "Unix"
Conditions = [ """"type":"wazuh-alerts"""", """session opened for user""","""su:""", """(uid=""" ]
DupFields = [
"host->dest_host"
"description->event_name"
]
ParserVersion = "v1.0.0"


}
```
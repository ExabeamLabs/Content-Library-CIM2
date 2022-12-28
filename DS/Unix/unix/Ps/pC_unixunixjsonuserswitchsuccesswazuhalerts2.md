#### Parser Content
```Java
{
Name = unix-unix-json-user-switch-success-wazuhalerts-2
Product = "Unix"
Vendor = "Unix"
Conditions = [
  """"type":"wazuh-alerts""""
  """"rule.description":"User successfully changed UID.""""
]
DupFields = [
  "host->dest_host"
  "description->event_name"
]
ParserVersion = "v1.0.0"


}
```
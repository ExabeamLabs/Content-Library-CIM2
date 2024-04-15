#### Parser Content
```Java
{
Name = "unix-unix-json-endpoint-authentication-fail-userloginfail"
Product = "Unix"
Vendor = "Unix"
Conditions = [
""""type":"wazuh-alerts""""
""""rule.description":"PAM: User login failed.""""
]
DupFields = [
"host->dest_host"
"description->event_name"
]
ParserVersion = "v1.0.0"


}
```
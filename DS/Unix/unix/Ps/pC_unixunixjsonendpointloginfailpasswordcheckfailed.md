#### Parser Content
```Java
{
Name = "unix-unix-json-endpoint-login-fail-passwordcheckfailed"
Product = "Unix"
Vendor = "Unix"
Conditions = [
""""type":"wazuh-alerts""""
""""rule.description":"unix_chkpwd: Password check failed.""""
]
DupFields = [
"host->dest_host"
"description->event_name"
]
ParserVersion = "v1.0.0"


}
```
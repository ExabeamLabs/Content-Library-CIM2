#### Parser Content
```Java
{
Name = microsoft-windows-json-app-login-wazuhalerts
Conditions = [
  """"type":"wazuh-alerts""""
  """"rule.description":"MS SQL Server Logon Success."""
]
ParserVersion = "v1.0.0"

wazuh-common-fields.Fields} [
    """"predecoder.hostname":"({host}[^"]+)""",
    """"data.dstuser":"({dest_user}[^"]+)""",
    """"agent\.labels\.network\.ipv4\.primary":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  ParserVersion = "v1.0.0"
  DupFields=["host->dest_host", "description->event_name"
}
```
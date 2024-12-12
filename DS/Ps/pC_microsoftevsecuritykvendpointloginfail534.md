#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-fail-534"
Conditions = [
  """LogType="WLS""""
  """EventID="534""""
]
ParserVersion = "v1.0.0"

netapp-json-windows-events.Fields} [
    """'Computer':\s+'({host}[\w\-\.]+)""",
    """'IpAddress':\s+'({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  DupFields = [ "dest_user->user","dest_domain->domain","host->dest_host" 
}
```
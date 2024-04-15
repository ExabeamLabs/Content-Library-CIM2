#### Parser Content
```Java
{
Name = "citrix-endpointmgmt-kv-app-activity-success-audit"
Vendor = "Citrix"
Product = "Citrix Endpoint Management"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
  """Original Address="""
  """XMS - """
  """Audit ["""
  """event.action="""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d)"""
  """Original Address=({host}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})"""
  """app.name="({app}[^"]+)""""
  """client.ip="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """device.id="({src_host}[^"]+)""""
  """event.action="({operation}[^"]+)""""
  """event.status="({result}[^"]+)""""
  """http.user-agent="({user_agent}[^"]+)""""
  """session.id="({session_id}[^"]+)""""
  """push.user="(({email_address}[^@"]+?@[^"]+)|(({domain}[^,\\]+)[\\]+({user}[^"]+))|({=user}[^"]+))"""
  """user.id="(({email_address}[^@"]+?@[^"]+)|(({domain}[^,\\]+)[\\]+({user}[^"]+))|({=user}[^"]+))"""
  """arg1":"({additional_info}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```
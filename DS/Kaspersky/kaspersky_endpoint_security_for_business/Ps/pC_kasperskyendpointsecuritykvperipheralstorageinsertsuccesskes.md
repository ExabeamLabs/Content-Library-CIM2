#### Parser Content
```Java
{
Name = kaspersky-endpointsecurity-kv-peripheral-storage-insert-success-kes
Vendor = "Kaspersky"
Product = "Kaspersky Endpoint Security for Business"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """ KES|"""
  """ tdn=""""
  """ hdn=""""
  """Device VID and PID:"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ) ({host}[\w\-.]+) KES\|"""
  """hip="({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """hdn="({dest_host}[^"]+)"""
  """Device type\/Bus type:\s*({device_type}[^"\\]+)"""
  """Device ID:\s*({device_id}.+)&\d+"""
  """User:\s*(({domain}[^"\\]+)\\+)?({user}[^\\\s"]+)"""
  """Result\\Decision:\s*({action}[^"\\]+)"""
  """Operation:\s*({operation}[^\\"]+)"""
  """etdn="({operation_details}[^"]+)"""
]
DupFields = [
  "operation_details->alert_name"
  "action->alert_type"
  "operation->result"
]
ParserVersion = "v1.0.0"


}
```
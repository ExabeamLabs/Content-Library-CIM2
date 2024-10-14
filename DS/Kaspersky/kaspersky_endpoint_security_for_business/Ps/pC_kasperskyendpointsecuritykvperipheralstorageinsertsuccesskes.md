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
  """hip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """hdn="({dest_host}[^"]+)"""
  """Device type\/Bus type:\s*({device_class}[^"\\]+)"""
  """Device ID:\s*({device_id}.+)&\d+"""
  """User:\s*(({domain}[^"\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """Result\\Decision:\s*({action}[^"\\]+)"""
  """Operation:\s*({operation}[^\\"]+)"""
  """etdn="({operation_details}[^"]+)"""
  """VID and PID:\s*VEN_({device_vid}[^&]+)&(amp;)?PROD_({device_pid}[^\\&]+)"""
]
DupFields = [
  "operation_details->alert_name"
  "action->alert_type"
  "operation->result"
]
ParserVersion = "v1.0.0"


}
```
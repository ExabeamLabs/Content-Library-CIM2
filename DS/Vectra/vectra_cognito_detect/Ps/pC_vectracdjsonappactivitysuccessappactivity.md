#### Parser Content
```Java
{
Name = "vectra-cd-json-app-activity-success-appactivity"
Product = "Vectra Cognito Detect"
Vendor = "Vectra"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """vectra_timestamp"""
  """reason"""
  """action"""
  """src_name"""
]
Fields = [
  """({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
  """({app}vectra)"""
  """"*dvchost"*:\s*"+({host}[^"]+)"""
  """"*src_name"*:\s*"+({src_host}[^"]+)"""
  """"*dest_name"*:\s*"+({dest_host}[^"]+)"""
  """"*src_ip"*:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"*action"*:\s*"+({operation}[^"]+)"""
  """"*dest_ip"*:\s*"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """"*reason"*:\s*"+({result}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```
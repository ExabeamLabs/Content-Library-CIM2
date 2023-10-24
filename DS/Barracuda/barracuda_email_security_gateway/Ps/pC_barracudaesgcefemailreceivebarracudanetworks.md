#### Parser Content
```Java
{
Name = barracuda-esg-cef-email-receive-barracudanetworks
Vendor = "Barracuda"
Product = "Barracuda Email Security Gateway"
TimeFormat = "epoch"
Conditions = [
  """Barracuda Networks"""
  """Email Security Gateway"""
]
Fields = [
  """dvc=({host}[^\s]+)"""
  """\srt=({time}\d{13})""" 
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """act=({action}[^\s]+)"""
  """flexString1=({operation}[^\:]+):({result}\d+)"""
  """\|({alert_severity}[^\|]+)\|\s*event"""
  """suser=(-|({src_email_address}[^\s]+))"""
  """duser=(-|({dest_email_address}[^\s]+))"""
  """reason=({alert_name}\d+)"""
]
ParserVersion = "v1.0.0"


}
```
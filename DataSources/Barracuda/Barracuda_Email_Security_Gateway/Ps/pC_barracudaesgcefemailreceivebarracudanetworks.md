#### Parser Content
```Java
{
Name = barracuda-esg-cef-email-receive-barracudanetworks
Vendor = "Barracuda"
Product = "Barracuda Email Security Gateway"
TimeFormat = "epoch_sec"
Conditions = [
  """Barracuda Networks"""
  """Email Security Gateway"""
]
Fields = [
  """dvc=({host}[^\s]+)"""
  """rt=({time}[^\s]+)"""
  """src=({src_ip}[^\s]+)"""
  """act=({action}[^\s]+)"""
  """flexString1=({operation}[^\:]+):({result}\d+)"""
  """\|({alert_severity}[^\|]+)\|\s*event"""
  """suser=(-|({email_address}[^\s]+))"""
  """duser=(-|({dest_email_address}[^\s]+))"""
  """reason=({alert_name}\d+)"""
]
ParserVersion = "v1.0.0"


}
```
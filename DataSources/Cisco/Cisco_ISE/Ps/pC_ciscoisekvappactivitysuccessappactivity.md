#### Parser Content
```Java
{
Name = cisco-ise-kv-app-activity-success-appactivity
Vendor = "Cisco"
Product = "Cisco ISE"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """_TACACSAdmin"""
  """service="""
  """cmd="""
]
Fields = [
  """User-Name =(?!host\/)(?:[a-f0-9]{12}|({user}[^,]+))"""
  """NAS-IP-Address=(::ffff:)?({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """cmd=({operation}[^,]+)"""
  """_({app}TACACSAdmin)"""
  """priv-lvl=({privileges}[^,]+)"""
  """task_id=\w+@(::ffff:)?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
]
ParserVersion = "v1.0.0"


}
```
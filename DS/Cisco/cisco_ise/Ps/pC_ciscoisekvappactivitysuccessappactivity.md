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
  """User-Name =(?!host\/)(?:[a-f0-9]{12}|({user}[\w\.\-]{1,40}\$?))"""
  """NAS-IP-Address=(::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """cmd=({operation}[^,]+)"""
  """_({app}TACACSAdmin)"""
  """priv-lvl=({privileges}[^,]+)"""
  """task_id=\w+@(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```
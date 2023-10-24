#### Parser Content
```Java
{
Name = "hp-arubacpm-kv-endpoint-login-success-authsuccessfull"
Vendor = "HP"
Product = "Aruba ClearPass Policy Manager"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """Authentication Successful"""
  """method="""
  """server="""
  """authmgr"""
]
Fields = [
  """({time}\d{4}-\d{2}-\d{2}T\d\d:\d\d:\d\d)\+"""
  """\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\+\d{2}:\d{2}\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\s+({host}[^\s]+)\s+authmgr\["""
  """(authmgr|stm)\[({event_code}\d+)\]"""
  """username=((({domain}[^\\\s\@]+)\\|({user_type}host)\/)?({email_address}[^\s\@]+\@({email_domain}[^\s]+))?({src_mac}([0-9a-fA-F]{1,2}[.:-]){5}([0-9a-fA-F]{1,2}))?(({user}[\w\.\-]{1,40}\$?)?(\/)?({=domain}[^\\\s\@]+)?))"""
  """MAC=({src_mac}[a-fA-F\d:]+)"""
  """user=({src_mac}[a-fA-F\d:]+)"""
  """Authentication result=({event_name}Authentication Successful)"""
  """method=({auth_type}[^\,\s]+)"""
  """server=({auth_server}[\w\d]+)"""
]
ParserVersion = "v1.0.0"


}
```
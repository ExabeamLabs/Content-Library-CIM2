#### Parser Content
```Java
{
Name = "checkpoint-ngfw-kv-vpn-login-network"
Vendor = "Check Point"
Product = "Check Point NGFW"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """ProductName ="Connectra"""
  """ProductFamily="Network""""
  """status="""
  """vpn_category="""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\S+\s({host}\d+.\d+.\d+.\d+)\s"""
  """src=\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """dst=\"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """proto=\"({protocol}[^\"]+)"""
  """sport_svc=\"({src_port}\d+)"""
  """svc=\"({dest_port}\d+)"""
  """tunnel_protocol=\"+({tunnel_protocol}[^\"]+)"""
  """\Wreason=\"+({failure_reason}.+?)\s*\"+ latitude="""
  """\WUser=\"+(({full_name}[^\(]+)\s\()?(({email_address}[^@\"]+@[^\"]+)|({user}[\w\.\-]{1,40}\$?))\)?\"+ auth_method="""
]
ParserVersion = "v1.0.0"


}
```
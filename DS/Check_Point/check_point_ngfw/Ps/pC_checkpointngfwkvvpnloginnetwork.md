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
  """src=\"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """dst=\"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """proto=\"({protocol}[^\"]+)"""
  """sport_svc=\"({src_port}\d+)"""
  """svc=\"({dest_port}\d+)"""
  """tunnel_protocol=\"{1,20}({tunnel_protocol}[^\"]+)"""
  """\Wreason=\"{1,20}({failure_reason}.+?)\s*\"{1,20} latitude="""
  """\WUser=\"{1,20}(({full_name}[^\(]+)\s\()?(({email_address}[^@\"]+@[^\"]+)|({user}[^\"\)]+))\)?\"{1,20} auth_method="""
]
ParserVersion = "v1.0.0"


}
```
#### Parser Content
```Java
{
Name = "secureauth-login-cef-endpoint-login-success-20990"
Vendor = "SecureAuth"
Product = "SecureAuth Login"
TimeFormat = "epoch"
Conditions = [
  """|SecureAuth|"""
  """|ID20990|Success|"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sflexString1=({host}[^\s]+)"""
  """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\ssuser=({user}.+?)\s+\w+="""
  """requestClientApplication=(?:-|({user_agent}[\s]+))"""
]
ParserVersion = "v1.0.0"


}
```
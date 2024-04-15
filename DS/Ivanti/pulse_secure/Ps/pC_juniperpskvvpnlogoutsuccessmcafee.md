#### Parser Content
```Java
{
Name = "juniper-ps-kv-vpn-logout-success-mcafee"
Vendor = "Ivanti"
Product = "Pulse Secure"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|McAfee|"""
  """SecureAccess"""
  """User Session Ended"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\sdeviceTranslatedAddress=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\ssuser=({user}.+?)\s*$"""
  """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```
#### Parser Content
```Java
{
Name = "fidelis-fxps-kv-email-receive-success-fidelisxps"
Vendor = "Fidelis"
Product = "Fidelis XPS"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """Fidelis XPS"""
  """Protocol="""
  """Sensor="""
]
Fields = [
  """Time=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """\w+ \d+ \d\d:\d\d:\d\d\s({host}[\w\-.]+)\sProduct"""
  """\sDestIP="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
  """From=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)\s"""
  """To=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """To=({email_recipients}[^\n\s]+)"""
  """SrcIP="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """Severity="({alert_severity}[^"]+)""""
  """Filename="(?!(<n\/a>))({email_attachments}[^"]+)""""
  """Filename="(?!(<n\/a>))({email_attachment}[^\.]+(\.({file_ext}[^"]+))?)("|,)"""
  """Protocol="({protocol}[^"]+)""""
  """Rule="({alert_type}[^"]+)""""
  """SrcPort="({src_port}\d+)""""
  """DestPort="({dest_port}\d+)""""
]
ParserVersion = "v1.0.0"


}
```
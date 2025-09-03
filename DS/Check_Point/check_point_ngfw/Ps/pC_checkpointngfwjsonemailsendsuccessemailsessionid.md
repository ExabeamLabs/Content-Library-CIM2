#### Parser Content
```Java
{
Name = "checkpoint-ngfw-json-email-send-success-emailsessionid"
Vendor = "Check Point"
Product = "Check Point NGFW"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """CheckPoint"""
  """from:"""
  """to:"""
  """email_session_id"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ) ({host}[\w.\-]+) CheckPoint """
  """\Wifname:"({src_interface}[^"]+)"""
  """\Worigin:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wfrom:"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """\Wto:"({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^"]*?)""""
  """\Wemail_session_id:"({message_id}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```
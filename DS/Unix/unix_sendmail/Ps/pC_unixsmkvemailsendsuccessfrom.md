#### Parser Content
```Java
{
Name = unix-sm-kv-email-send-success-from
Vendor = "Unix"
Product = "Unix Sendmail"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
  """ TRANSMIT["""
  """from=<"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)\s+({host}\S+)\s+TRANSMIT\[.*?\]:\s*({alert_id}[^:]+?)\s*:"""
  """\sfrom=<({src_email_address}[^@]+?@.+?)>"""
  """\ssize=({bytes}\d+)"""
  """\snrcpts=({num_recipients}\d+)"""
  """\sproto=({protocol}[^,]+)"""
  """\srelay=({dest_host}[\w\-.]+)\s*\[({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```
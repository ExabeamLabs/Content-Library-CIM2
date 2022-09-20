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
  """\sfrom=<({email_address}[^@]+?@.+?)>"""
  """\ssize=({bytes}\d+)"""
  """\snrcpts=({num_recipients}\d+)"""
  """\sproto=({protocol}[^,]+)"""
  """\srelay=({dest_host}[\w\-.]+)\s*\[({dest_ip}[a-fA-F:\d.]+)"""
]
ParserVersion = "v1.0.0"


}
```
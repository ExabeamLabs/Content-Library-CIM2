#### Parser Content
```Java
{
Name = unix-sm-kv-email-send-success-to
Vendor = "Unix"
Product = "Unix Sendmail"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
  """ TRANSMIT["""
  """to=<"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)\s+({host}\S+)\s+TRANSMIT\[.*?\]:\s*({alert_id}[^:]+?)\s*:"""
  """\sto=<({dest_email_address}[^@]+?@.+?)>"""
  """\sto=({email_recipients}.+?)(,\s+\[more\])?(,\s+\w+=|\s*$)"""
  """\smailer=({protocol}[^,]+)"""
  """\srelay=({dest_host}[\w\-.]+)\s*\[({dest_ip}[a-fA-F:\d.]+)"""
  """\sdsn=({result}[^,]+)"""
]
ParserVersion = "v1.0.0"


}
```
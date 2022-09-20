#### Parser Content
```Java
{
Name = cisco-secureemail-cef-email-send-success-logevent
Vendor = "Cisco"
Product = "Cisco Secure Email"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """CEF"""
  """ Email Security Appliance|"""
  """ ESAMID="""
]
Fields = [
  """suser=({email_address}[^\s]+)"""
  """\sduser=({email_recipients}[^\s]+)\s+(\w+=|$)"""
  """\sduser=({dest_email_address}[^,\s;]+)"""
  """sourceAddress=({src_ip}[A-Fa-f:\d.]+)"""
  """ESAMID=({alert_id}\d+)"""
  """\|Cisco\|([^\|]*\|){2}({alert_type}[^\|]+)"""
  """\|Cisco\|([^\|]*\|){3}({alert_name}[^\|]+)"""
  """\|Cisco\|([^\|]*\|){4}({alert_severity}[^\|]+)"""
  """deviceDirection=({direction}\d)"""
  """\Wact=({action}[^=]+?)\s*\w+="""
]
ParserVersion = "v1.0.0"


}
```
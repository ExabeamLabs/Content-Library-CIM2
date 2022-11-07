#### Parser Content
```Java
{
Name = cisco-secureemail-cef-email-receive-fail-secureemailgateway
  Vendor = Cisco
  Product = Cisco Secure Email
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CEF:""" , """ Secure Email Gateway Virtual|""", """ ESAMID=""", """|Cisco|""" ]
  Fields = [
    """suser=({email_address}[^\s]+)""",
    """\sduser=({email_recipients}[^\s]+)\s+(\w+=|$)""",
    """\sduser=({email_recipients}[^,\s;]+)""",
    """sourceAddress=({src_ip}[A-Fa-f:\d.]+)""",
    """sourceHostName =({src_host}[^\s]+)""",
    """msg='\s*({email_subject}[^']+')""",
    """ESAMID=({alert_id}\d+)""",
    """\|Cisco\|([^\|]*\|){2}({alert_type}[^\|]+)""",
    """\|Cisco\|([^\|]*\|){3}({alert_name}[^\|]+)""",
    """\|Cisco\|([^\|]*\|){4}({alert_severity}[^\|]+)""",
    """deviceDirection=({direction}\d)""",
    """\Wact=({action}[^=]+?)\s*\w+="""
  ]
  DupFields = [ "action->result" ]
  ParserVersion = "v1.0.0"


}
```
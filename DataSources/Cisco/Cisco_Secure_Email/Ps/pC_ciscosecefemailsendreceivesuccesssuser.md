#### Parser Content
```Java
{
Name = cisco-se-cef-email-send-receive-success-suser
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Secure Email
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CEF""" , """Email Security Virtual Appliance""", """suser=""" ]
  Fields = [ 
    """suser=({email_address}[^\s]+)""",
    """\sduser=({email_recipients}[^\s]+)\s+(\w+=|$)""",
    """\sduser=({dest_email_address}[^,\s;]+)""",
    """sourceAddress=({src_ip}[^\s]+)""",
    """msg='({email_subject}[^']+)'""",
    """ESAMID=({alert_id}\d+)""",
    """cfp1=(not enabled|({alert_severity}[^\s]+))""",
    """\|Cisco\|([^\|]*\|){2}({alert_type}[^\|]+)""",
    """\|Cisco\|([^\|]*\|){3}({alert_name}[^\|]+)""",
    """\|Cisco\|([^\|]*\|){4}({alert_severity}[^\|]+)"""
    """deviceDirection=({direction}\d)"""
  ]
 

}
```
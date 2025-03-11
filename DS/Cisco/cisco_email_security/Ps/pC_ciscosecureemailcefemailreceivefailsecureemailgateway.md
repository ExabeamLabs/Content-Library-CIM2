#### Parser Content
```Java
{
Name = cisco-secureemail-cef-email-receive-fail-secureemailgateway
  Vendor = Cisco
  Product = Cisco Email Security
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "MMM dd HH:mm:ss"]
  Conditions = [ """CEF:""" , """ Secure Email Gateway Virtual|""", """ ESAMID=""", """|Cisco|""" ]
  Fields = [
    """({time}\w+\s\d\d\s\d\d:\d\d:\d\d(\s\d\d\d\d)?)\s(\d+|({host}[\w\-\.]+))\s""",
    """\sstart(Time)?=(\w+\s)?({time}\w+\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)\s""",
    """suser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """\sduser=({email_recipients}[^\s]+)\s+(\w+=|$)""",
    """\sduser=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """sourceAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
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
#### Parser Content
```Java
{
Name = cisco-se-cef-email-send-receive-esafriendlyfrom
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Secure Email
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """CEF""" , """|Cisco|""", """Email Security Virtual Appliance""", """ESA_CONSOLIDATED_LOG_EVENT""", """ESAFriendlyFrom""" ]
  Fields = [
    """({time}\w{3}\s+\d{1,2}\s+\d\d:\d\d:\d\d\s+\d\d\d\d)"""
    """ESAFriendlyFrom=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-\\]+)*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s]+))""",
    """ESAFriendlyFrom="({full_name}[^"\(\)]+[\s,]+[^"\(\)]+)"""
    """ESAReplyTo=({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\s]*)\s+(\w+=|$)""",
    """msg='\s*(\\=\?[^']+|({email_subject}[^']+?))\s*'""",
    """ESAMID=({alert_id}\d+)""",
    """cfp1=(not enabled|({alert_severity}[^\s]+))""",
    """\|Cisco\|([^\|]*\|){2}({alert_type}[^\|]+)""",
    """\|Cisco\|([^\|]*\|){3}({alert_name}[^\|]+)""",
    """\|Cisco\|([^\|]*\|){4}({alert_severity}[^\|]+)"""
    """deviceDirection=({direction}\d)"""
    """\s+ESAAttachmentDetails=\{\'(unknown|({email_attachment}[^']+))\'""",
    """ESAAttachmentDetails=({additional_info}[^"=]+?)\s*ESAFriendlyFrom=""",
    """ESAMsgSize=({bytes}\d+)\s"""
    """ESAMFVerdict=({result}[\w\.\-]+)"""
    """\Wact=({action}[^=]+?)\s*\w+="""
  ]


}
```
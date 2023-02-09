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
    """suser=(({sender}[^\s@]+@[^\s\.@]+\.[^\s]+)|({user}[^\s@]+)@({domain}[^\s]+))""",
    """\sduser=({email_recipients}({dest_email_address}[^,\s;@]+@[^,\s;\.\[]+\.[^,\s;]+)[^\s]*)\s+(\w+=|$)""",
    """\sduser=({dest_email_address}[^,\s;]+)""",
    """sourceAddress=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """msg='\s*(\\=\?[^']+|({email_subject}[^']+?))\s*'""",
    """ESAMID=({alert_id}\d+)""",
    """cfp1=(not enabled|({alert_severity}[^\s]+))""",
    """\|Cisco\|([^\|]*\|){2}({alert_type}[^\|]+)""",
    """\|Cisco\|([^\|]*\|){3}({alert_name}[^\|]+)""",
    """\|Cisco\|([^\|]*\|){4}({alert_severity}[^\|]+)"""
    """deviceDirection=({direction}\d)"""
    """\s+ESAAttachmentDetails=\{\'(unknown|({email_attachment}[^']+))\'""",
    """ESAAttachmentDetails=({additional_info}[^"]+?)\s*ESAFriendlyFrom=""",
    """ESAMsgSize=({bytes}\d+)\s"""
  ]
 

}
```
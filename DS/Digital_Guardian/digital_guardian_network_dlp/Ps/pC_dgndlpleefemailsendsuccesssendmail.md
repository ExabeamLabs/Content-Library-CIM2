#### Parser Content
```Java
{
Name = dg-ndlp-leef-email-send-success-sendmail
  ParserVersion = v1.0.0
  Vendor = Digital Guardian
  Product = Digital Guardian Network DLP
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ 
"""LEEF:""" 
"""|Digital Guardian|Digital Guardian|""" 
"""DigitalGuardian-Events"""
"""|Send Mail|"""
]
  Fields = [
    """devTime=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """({host}[\w\-.]+) LEEF:""",
    """accountName =(({domain}[^\\]+)\\+)?({user}[^\\\s]+?)\s*(\w+=|$)""",
    """IdentHostName =(({domain}[^\\])+\\+)?({dest_host}[\w\-.]+?)\s*(\w+=|$)""",
    """src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """EmailSender=({src_email_address}.+?)\s*(\w+=|$)""",
    """usrName =(?![^\s]+@[^\s]+)(({domain}[^\\]+)\\+)?({user}[^\\\s@]+)\s*(\w+=|$)""",
    """usrName =(?=[^\s]+@[^\s]+)({email_address}[^\s@]+@[^\s]+)""",
    """EmailRecipient=(|({dest_email_address}[^\s,;]+))""",
    """EmailRecipient=(|({email_recipients}.+?))\s*(\w+=|$)""",
    """EmailSubject=(|({email_subject}.+?))\s*(\w+=|$)""",
    """sev=({alert_severity}\d+)""",
    """srcBytes=({bytes}\d+)""",
    """FileSizeMB=({bytes}\d+)""",
    """FileSize({bytes_unit}MB)""",
    """DestinationFile=(|({email_attachments}[^\.]+\.({file_ext}.+?)))\s*(\w+=|$)""",
    """EmailRecipient=({email_recipients}[^\s@]+@[^\s@]+)"""
  ]


}
```
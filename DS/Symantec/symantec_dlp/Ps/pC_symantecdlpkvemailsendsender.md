#### Parser Content
```Java
{
Name = symantec-dlp-kv-email-send-sender
  Vendor = Symantec
  Product = Symantec DLP
  TimeFormat = "MMMM dd, yyyy HH:mm:ss a"
  Conditions = [ """Policy_Violated:_""", """Subject:_""", """Email_Blocked:""", """Sender:_""", """Attachment:_""" ]
  Fields = [
    """Incident_Date:\_({time}\w+\s\d\d,\s\d\d\d\d\s\d{1,2}:\d{1,2}:\d{1,2}\s((?i)am|pm))"""
    """\s\d\d\s\d\d:\d\d:\d\d\s({host}[\w\.\-]+)\s""",
    """\sEmail_Blocked:\_({result}[^\s,]+)""",
    """\sSender:\_({src_email_address}[^\s@:]+@[^\s\.:]+\.[^\s:]+)""",
    """\sRecipient:\_({recipients}({dest_email_address}[^\s@:,]+@[^\s\.:,]+\.[^\s:,]+)[^:]*?)\sSubject:""",
    """Subject:\_(N\/A|({email_subject}[^\n]+?))\s*Attachment:""",
    """Policy_Violated:\_({alert_name}[^:]+?)(\s\-\s|\sSender:)""",
    """({alert_type}Policy_Violated)""",
    """Attachment:\_(N\/A|Unknown|({attachment}[^\n]+?\.\w+?))\s""",
    """Attachment:\_(N\/A|Unknown|({email_attachments}[^\n]+?))\s+Incident_Link:""",
    """Message_ID:\_({alert_id}[^\s]+)"""
    """Incident_Link:\_({additional_info}[^\s"]+)\s*"""
  ]
  DupFields = ["alert_id->message_id"]
  ParserVersion = v1.0.0


}
```
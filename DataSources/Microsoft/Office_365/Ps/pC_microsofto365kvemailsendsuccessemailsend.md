#### Parser Content
```Java
{
Name = microsoft-o365-kv-email-send-success-emailsend
  Vendor = Microsoft
  Product = Office 365
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """DateStamp=""", """MessageTraceID=""" ]
  Fields = [
    """Received="({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
    """Index="({alert_id}\d+)"""",
    """Status="({result}[^"]+)"""",
    """Subject="({email_subject}[^"]+)"""",
    """SenderAddress="({email_address}[^"]+)"""",
    """RecipientAddress="({email_recipients}[^"]+)"""",
    """RecipientAddress="({external_address}[^",]+)"""",
    """FromIP="({src_ip}[^"]+)"""",
    """ToIP="({dest_ip}[^"]+)"""",
    """Size="({bytes}\d+)"""",
    """({alert_name}Office365)""",
    """({alert_type}o365_mail)""",
  ]
  ParserVersion = "v1.0.0"


}
```
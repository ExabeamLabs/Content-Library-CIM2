#### Parser Content
```Java
{
Name = microsoft-o365-kv-email-send-success-emailsend
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """DateStamp=""", """MessageTraceID=""" ]
  Fields = [
    """Received="({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
    """Index="({alert_id}\d+)"""",
    """Status="({result}[^"]+)"""",
    """Subject="({email_subject}[^"]+)"""",
    """SenderAddress="({src_email_address}[^"]+)"""",
    """RecipientAddress="({email_recipients}[^"]+)"""",
    """RecipientAddress="({external_address}[^",]+)"""",
    """FromIP="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """ToIP="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """Size="({bytes}\d+)"""",
    """({alert_name}Office365)""",
    """({alert_type}o365_mail)""",
  ]
  ParserVersion = "v1.0.0"


}
```
#### Parser Content
```Java
{
Name = mcafee-ep-kv-email-send-success-emailprotection
  Vendor = McAfee
  Product = McAfee Email Protection
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """OUTGOING_EMAIL""", """DLP: Email Protection""" ]
  Fields = [
     """UserName ="({email_domain}[^\\]+)\\({user}[^"]+)"""",
     """ComputerName ="({src_host}[^"]+)"""",
     """EMAIL_RECIPIENT.+?>({dest_email_address}[^<]+)<""",
     """EMAIL_SUBJECT.+?>({email_subject}[^<]+)<""",
     """FILE_NAME.+?>({email_attachment}[^<]+)<""",
     """FILE_NAME.+?size="({bytes}\d+)""",
     """UTCTime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
     """Evidence="({email_recipients}[^=]+@[^,]+),""",
  ]
  ParserVersion = "v1.0.0"


}
```
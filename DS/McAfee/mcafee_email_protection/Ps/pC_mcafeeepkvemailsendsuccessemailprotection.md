#### Parser Content
```Java
{
Name = mcafee-ep-kv-email-send-success-emailprotection
  Vendor = McAfee
  Product = McAfee Email Protection
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """OUTGOING_EMAIL""", """DLP: Email Protection""" ]
  Fields = [
     """UserName ="({domain}[^\\]+)\\({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
     """ComputerName ="({src_host}[^"]+)"""",
     """EMAIL_RECIPIENT.+?>({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|\<]+))<""",
     """EMAIL_SUBJECT.+?>({email_subject}[^<]+)<""",
     """FILE_NAME.+?>({email_attachment}[^<]+)<""",
     """FILE_NAME.+?size="({bytes}\d+)""",
     """UTCTime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
     """Evidence="({email_recipients}[^=]+@[^,]+),""",
  ]
  ParserVersion = "v1.0.0"


}
```
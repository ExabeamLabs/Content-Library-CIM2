#### Parser Content
```Java
{
Name = microsoft-m365auditlogs-kv-email-send-emailsend
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = M365 Audit Logs
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"MessageTraceId":"""", """"SenderAddress":"""", """"RecipientAddress":"""", """cs6=""" ]
  Fields = [
    """cs6=.*?"StartDate":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)""",
    """"Subject":"\s*(({email_subject}.*?\\.*?)|({=email_subject}[^"]+?))\s*",""",
    """cs6=.*?"Direction":"({direction}[^"]+)"""",
    """cs6=.*?"SenderAddress":"({email_address}[^",]+)"""",
    """cs6=.*?"RecipientAddress":"({email_recipients}[^"]+)"""",
    """cs6=.*?"RecipientAddress":"({dest_email_address}[^"\s,;]+)""",
    """cs6=.*?"Size":"?({bytes}\d+)""",
    """cs6=.*?"Status":"({result}[^"]+)"""",
    """cs6=.*?"ToIP":"?(?:null|({dest_ip}[a-fA-F\d.:]+))""",
    """cs6=.*?"FromIP":"?(?:null|({src_ip}[a-fA-F\d.:]+))""",
    """cs6=.*?"EventType":"({alert_type}[^"]+)"""",
    """cs6=.*?"MessageTraceId":"({message_id}[^"]+)"""",
  ]
  DupFields = [ "alert_type->alert_name" ]


}
```
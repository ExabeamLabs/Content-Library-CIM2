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
    """cs6=.*?"ToIP":"?(?:null|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """cs6=.*?"FromIP":"?(?:null|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """cs6=.*?"EventType":"({alert_type}[^"]+)"""",
    """cs6=.*?"MessageTraceId":"({message_id}[^"]+)"""",
  ]
  DupFields = [ "alert_type->alert_name" ]


}
```
#### Parser Content
```Java
{
Name = microsoft-o365-sk4-email-receive-success-inbound
  Vendor = Microsoft
  Product = Microsoft 365
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"Direction":"Inbound"""", """"MessageTraceId":"""", """"SenderAddress":""", """"RecipientAddress":"""" ]
  Fields = [
    """"Date":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)""",
    """"Subject":"({email_subject}[^"]+)"""",
    """"Direction":"({direction}[^"]+)"""",
    """"SenderAddress":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """"RecipientAddress":"({email_recipients}[^"]+)"""",
    """"MessageSize":"?({bytes}\d+)""",
    """"MessageTraceId":"({message_id}[^"]+)"""",
    """"MessageId":"({message_id}[^"]+)"""",
    """"EventType":"({alert_type}[^"]+)""""
    """"Action":"({action}[^"]+)"""
    """"BulkComplaintLevel":"({spam_score}[^"]+)""""
  ]
  DupFields = [ "alert_type->alert_name", "alert_type->result", "email_recipients->dest_email_address" ]


}
```
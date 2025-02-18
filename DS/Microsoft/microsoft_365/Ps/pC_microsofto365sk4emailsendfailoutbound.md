#### Parser Content
```Java
{
Name = "microsoft-o365-sk4-email-send-fail-outbound"
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """"Direction":"Outbound""""
  """"MessageTraceId":""""
  """"SenderAddress":""""
  """"RecipientAddress":""""
]
Fields = [
  """"Date":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)"""
  """"Subject":"({email_subject}[^"]+)""""
  """"Direction":"({direction}[^"]+)""""
  """"SenderAddress":"({email_address}({email_user}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+)@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
  """"RecipientAddress":"({email_recipients}[^"]+)""""
  """"MessageSize":"?({bytes}\d+)"""
  """"MessageTraceId":"({message_id}[^"]+)"""",
  """"MessageId":"({message_id}[^"]+)"""",
  """"EventType":"({alert_type}[^"]+)""""
  """"Action":"({action}[^"]+)"""
]
DupFields = [
  "alert_type->alert_name"
  "alert_type->result"
]
ParserVersion = "v1.0.0"


}
```
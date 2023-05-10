#### Parser Content
```Java
{
Name = microsoft-exchange-json-email-success-5290
Vendor = Microsoft
Product = Microsoft Exchange
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"run_id":"""
  """"sender_address":"""
  """"recipient_domain":"""
]
Fields = [
  """"date_time":"({time}[^"]+)"""
  """"recipient_address":"({dest_email_address}[^"]+)"""
  """"email_direction":"({direction}[^"]+)"""
  """"message_subject":"({email_subject}.+?)\s*""""
  """"attachment_name":"(UNKNOWN|({email_attachment}[^"]+))"""
  """"sender_address":"({sender}[^"]+)"""
  """"total_bytes":({bytes}\d+)"""
  """"email_event":"({action}[^"]+)"""
]
DupFields = [
  "sender->user"
]
ParserVersion = "v1.0.0"


}
```
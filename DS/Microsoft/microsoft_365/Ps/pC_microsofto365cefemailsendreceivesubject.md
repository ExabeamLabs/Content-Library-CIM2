#### Parser Content
```Java
{
Name = microsoft-o365-cef-email-send-receive-subject
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
    """"MessageTraceId":"""",
    """"SenderAddress":"""",
    """"RecipientAddress":"""",
    """"Subject":"""",
    """CEF:"""
  ]
  Fields = [
    """"StartDate":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
    """"StartDate":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)""",
    """"Subject":"\s*({email_subject}.+?)\s*"}""",
    """"Subject":"\s*({email_subject}.+?)\s*",""",
    """"Direction":"({direction}[^"]+)"""",
    """"SenderAddress":"({sender}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)","""",
    """"RecipientAddress":"({email_recipients}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
    """"RecipientAddress":"({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
    """"Size":"?({bytes}\d+)""",
    """"Status":"({result}[^"]+)"""",
    """"ToIP":"?(?:null|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """"FromIP":"?(?:null|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """"EventType":"({alert_type}[^"]+)"""",
    """"MessageTraceId":"({message_id}[^"]+)"""",
    """"triggered-by":\{"user-email":"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
    """Category\s+\[({category}[^\]]+)\]"""
  ]
  DupFields = [ "alert_type->alert_name" ,"sender->orig_user" ]
 

}
```
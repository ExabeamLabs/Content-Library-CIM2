#### Parser Content
```Java
{
Name = microsoft-o365-cef-email-send-receive-subject
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Office 365
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
    """"SenderAddress":"({email_address}[^",]+)"""",
    """"RecipientAddress":"({email_recipients}[^"]+)"""",
    """"RecipientAddress":"({dest_email_address}[^"\s,;]+)""",
    """"Size":"?({bytes}\d+)""",
    """"Status":"({result}[^"]+)"""",
    """"ToIP":"?(?:null|({dest_ip}[a-fA-F\d.:]+))""",
    """"FromIP":"?(?:null|({src_ip}[a-fA-F\d.:]+))""",
    """"EventType":"({alert_type}[^"]+)"""",
    """"MessageTraceId":"({message_id}[^"]+)"""",
    """"triggered-by":\{"user-email":"({email_address}[^",]+)"""",
    """Category\s+\[({category}[^\]]+)\]"""
  ]
  DupFields = [ "alert_type->alert_name" ]
 

}
```
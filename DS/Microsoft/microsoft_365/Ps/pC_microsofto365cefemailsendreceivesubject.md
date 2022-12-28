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
    """"SenderAddress":"({email_address}[^@,]+@[^\.,]+\.[^\]\s",\|]+)","""",
    """"RecipientAddress":"({email_recipients}[^"]+)"""",
    """"RecipientAddress":"({dest_email_address}[^"\s,;]+)""",
    """"Size":"?({bytes}\d+)""",
    """"Status":"({result}[^"]+)"""",
    """"ToIP":"?(?:null|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """"FromIP":"?(?:null|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """"EventType":"({alert_type}[^"]+)"""",
    """"MessageTraceId":"({message_id}[^"]+)"""",
    """"triggered-by":\{"user-email":"({email_address}[^",]+)"""",
    """Category\s+\[({category}[^\]]+)\]"""
  ]
  DupFields = [ "alert_type->alert_name" ]
 

}
```
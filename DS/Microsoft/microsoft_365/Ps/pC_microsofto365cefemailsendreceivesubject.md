#### Parser Content
```Java
{
Name = microsoft-o365-cef-email-send-receive-subject
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss.SSS"]
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
    """"Subject":"\s*(|({email_subject}[^=]+?))\s*","\w+?":""",
    """"Direction":"({direction}[^"]+)"""",
    """"SenderAddress":"({src_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+(?<!local)(?<!loc))"""",
    """"RecipientAddress":"({email_recipients}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
    """"RecipientAddress":"({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
    """"Size":"?({bytes}\d+)""",
    """"Status":"({result}[^"]+)"""",
    """"ToIP":"?(?:null|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """"FromIP":"?(?:null|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """"EventType":"({alert_type}[^"]+)"""",
    """"MessageTraceId":"({message_id}[^"]+)"""",
    """"user-email":"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
    """Category\s+\[({category}[^\]]+)\]"""
    """"EventType":"({alert_subject}[^"]+)"""",
    """\ssourceServiceName =({alert_source}[^=]+)\s+\w+="""
    """fsize=({bytes}\d+)\s"""
  ]
  DupFields = [ "alert_type->alert_name" ,"src_email_address->orig_user" ,"src_email_address->email_address" ]
 

}
```
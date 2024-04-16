#### Parser Content
```Java
{
Name = microsoft-o365-cef-email-success-subject
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
    """CEF:""",
    """=Office 365""",
    """"MessageTraceId":"""",
    """"EventType":"""",
    """"RecipientAddress":""",
    """"SenderAddress":""",
    """"Direction":"""",
    """"Subject":""""
  ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z\s+[\w\-.]+\s+""",
    """filePath=<*({file_path}.+?)>*\s\w+=""",
    """fname=\s*({email_attachment}[^=]+?)\s*\w+=""",
    """"Domain":"({domain}[^"]+)""",
    """"Subject":"\s*({email_subject}[^",]+)\s*"""",
    """"MessageSize":({bytes}\d+)""",
    """"Direction":"({direction}[^"]+)""",
    """"SenderAddress":"({src_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+(?<!local)(?<!loc)(?<!localdomain))"""",
    """"RecipientAddress":"({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""",
    """"TransportRule":"({alert_name}[^"]+)""",
    """"EventType":"({alert_type}[^"]+)""",
    """Category\s+\[({category}[^\]]+)\]"""

 ]
 DupFields = [ 
  "email_attachment"->"file_name"
  "src_email_address->email_address"
 ]
 

}
```
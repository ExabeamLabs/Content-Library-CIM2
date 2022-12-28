#### Parser Content
```Java
{
Name = microsoft-o365-json-email-send-receive-internentmessageid
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ 
    """"Verdict":"Phish"""",
    """"Operation":"TIMailData"""",
    """"InternetMessageId":"""",
    """"Subject":""""
  ]
  Fields = [
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """({alert_type}Phish)""",
    """"DetectionMethod":"({alert_name}[^"]+)"""",
    """"eventTypeName":"({alert_name}[^"]+)"""",
    """"Recipients":\[?"({email_recipients}[^,;@]+@([^;,"]+))""",
    """"Id":"({alert_id}[^"]+)"""",
    """"SenderIp":"(0.0.0.0|({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?)))"""",
    """"SHA256":"({hash_md5}[^"]+)"""",
    """"Verdict":"({verdict}[^"]+)"""",
    """"Subject":"\s*({additional_info}[^,"]+?)[\s\t]*"(,|$)"""",
    """"Directionality":"({direction}[^",]+)"""",
    """"P2Sender":"([^@]+?\\=)?({email_address}[^@",\\=]+@[^",]+)"""",
    """"P1Sender":"([^@]+?\\=)?({email_address}[^@",\\=]+@[^",]+)"""",  
]
  DupFields = [ "email_recipients->dest_email_address","additional_info->email_subject" ]
 

}
```
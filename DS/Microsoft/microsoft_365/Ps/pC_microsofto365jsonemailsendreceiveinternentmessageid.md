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
    """"Recipients":\[?"({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"?\]?""", 
    """"Id":"({alert_id}[^"]+)"""",
    """"SenderIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"SHA256":"({hash_sha256}[^"]+)"""",
    """"Verdict":"({verdict}[^"]+)"""",
    """"Subject":"\s*({additional_info}({email_subject}[^"]+?))\s*",""",
    """"Directionality":"({direction}[^",]+)"""",
    """"P2Sender":"((([^@]+?\\=)+)?({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({email_user}[^"]+))"""",
    """"P1Sender":"((([^@]+?\\=)+)?({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({email_user}[^"]+))""""
    """AttachmentData\\?"*:\s*({attachment}\[\{\\?"*FileName\\?"+:\s*\\?"+({file_name}[^"\\]+)?\\?"+\,.+?FileType\\?"+:\s*\\?"+({file_ext}[^"\\;]+)?(;[^"\\;]+)?\\?"+\,.+?\])"""
    """"DeliveryAction":"({action}[^"]+)"""",
    """"Workload":\s*"({app}[^"]+)""""
    """"UserType":"*({user_type}[^,}"]+)"*"""
]
 

}
```
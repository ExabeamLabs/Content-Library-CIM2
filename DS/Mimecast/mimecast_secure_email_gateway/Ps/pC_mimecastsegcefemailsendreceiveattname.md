#### Parser Content
```Java
{
Name = mimecast-seg-cef-email-send-receive-attname
  ParserVersion = v1.0.0
  Vendor = Mimecast
  Product = Mimecast Secure Email Gateway
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ" ]
  Conditions = [ 
""""acc":""""
""""MsgId":""""
""""AttCnt":"""
""""AttNames":""" 
""""aCode":"""" 
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) [\w.\-]+ """,
    """"datetime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d+)"""",
    """"AttNames":\[({email_attachments}[^\]]+)\]""",
    """"aCode":"(|({alert_id}[^"]+?))"""",
    """"MsgSize":"*({bytes}\d+)""",
    """"Subject":"({email_subject}[^"]+?)\s*"""",
    """"Sender":"(<>|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))""",
    """"datetime":"({time}\d+-\d+-\d+T\d+:\d+:\d+-\d+)""",
    """"AttCnt":\s*"?({attachment_count}\d+)""",
    """"AttSize":\s*({attachment_size}\d+)""",
    """"Hld":"({result}[^"]+)""",
    """"MsgId":"<\\*"?({message_id}[^,]+)>"""",
    """"AttNames":\[["\\]+({email_attachment}[^"]+\.({file_ext}[^"]+?))["\\]+"""
    """"datetime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d+)"""",
    """"Act\\?":"({action}[^"]+)""""
  ]


}
```
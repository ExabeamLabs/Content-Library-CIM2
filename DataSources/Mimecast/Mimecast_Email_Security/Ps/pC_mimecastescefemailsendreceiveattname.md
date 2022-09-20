#### Parser Content
```Java
{
Name = mimecast-es-cef-email-send-receive-attname
  ParserVersion = v1.0.0
  Vendor = Mimecast
  Product = Mimecast Email Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ 
"""destinationServiceName =Mimecast Email Security"""
""""AttNames":""" 
""""aCode":"""" 
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) [\w.\-]+ """,
    """"AttNames":\[({email_attachments}[^\]]+)\]""",
    """"aCode":"(|({alert_id}[^"]+?))"""",
    """"acc":"({user}[^"]+)"""",
    """"MsgSize":"*({bytes}\d+)""",
    """"Subject":"({email_subject}[^"]+?)\s*"""",
    """"Sender":"(<>|({email_address}[^"]+))""",
    """"datetime":"({time}\d+-\d+-\d+T\d+:\d+:\d+-\d+)""",
    """"AttCnt":({attachment_count}\d+)""",
    """"AttSize":({attachment_size}\d+)""",
    """"Hld":"({result}[^"]+)""",
    """"MsgId":"<({message_id}[^"]+?)>"""",
    """"AttNames":\["({email_attachment}[^"]+\.({file_ext}[^"]+))"""
  ]


}
```
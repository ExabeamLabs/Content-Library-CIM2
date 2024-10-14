#### Parser Content
```Java
{
Name = mimecast-seg-cef-email-url
  Vendor = Mimecast
  Product = Mimecast Secure Email Gateway
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ 
""""fromUserEmailAddress":""" 
""""userEmailAddress":""""
""""ttpDefinition":""""
""""url":""""
""""scanResult":""""
""""subject"""" 
]
  Fields = [
    """"date":"({time}[^"]+)""",
    """"userEmailAddress":"({email_address}[^\s@"]+@[^\s@"]+)""",
    """"action":"({action}[^"]+)""",
    """"category":"(Unknown|({category}[^"]+))""",
    """"+fromUserEmailAddress"+:"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
    """"+url"+:"+({url}[^"]+)""",
    """"+ttpDefinition"+:"+({service_name}[^"]+)""",
    """"+subject"+:"+\s*({email_subject}.+?)\s*"+""",
    """"+route"+:"+({direction}[^"]+)""",
    """"+scanResult"+:"+({result}[^"]+)""",
    """"+scanResult"+:"+(clean|({failure_reason}[^"]+))""",
    """"sendingIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
    """"(messageId|MsgId)":"<({message_id}[^"]+)>"""",
    ]
    DupFields = ["email_address->dest_email_address","email_address->email_user"]


}
```
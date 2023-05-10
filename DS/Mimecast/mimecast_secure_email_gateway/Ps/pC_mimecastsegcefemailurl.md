#### Parser Content
```Java
{
Name = mimecast-seg-cef-email-url
  Vendor = Mimecast
  Product = Mimecast Secure Email Gateway
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ 
"""destinationServiceName =Mimecast Email Security""" 
""""userEmailAddress":""""
""""ttpDefinition":""""
""""url":""""
""""scanResult":""""
"""dproc="""
""""subject"""" 
]
  Fields = [
    """"date":"({time}[^"]+)""",
    """"userEmailAddress":"({email_address}[^\s@"]+@[^\s@"]+)""",
    """"action":"({action}[^"]+)""",
    """"category":"(Unknown|({category}[^"]+))""",
    """"+fromUserEmailAddress"+:"+({sender}[^"]+)""",
    """"+url"+:"+({url}[^"]+)""",
    """"+ttpDefinition"+:"+({service_name}[^"]+)""",
    """"+subject"+:"+\s*({email_subject}.+?)\s*"+""",
    """"+route"+:"+({direction}[^"]+)""",
    """"+scanResult"+:"+({url_verdict}[^"]+)""",
    """"+scanResult"+:"+(clean|({failure_reason}[^"]+))"""
    ]
    DupFields = ["email_address->dest_email_address","email_address->email_user"]


}
```
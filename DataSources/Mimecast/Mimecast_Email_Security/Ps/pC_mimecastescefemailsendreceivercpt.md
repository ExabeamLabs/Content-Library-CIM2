#### Parser Content
```Java
{
Name = mimecast-es-cef-email-send-receive-rcpt
  ParserVersion = v1.0.0
  Vendor = Mimecast
  Product = Mimecast Email Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ 
"""destinationServiceName =Mimecast Email Security""" 
""""Dir":""""
""""Sender":""""
""""Rcpt":""""
"""dproc=""" 
]
  Fields = [
    """"acc":"({host}[^",]+)"""",
    """"datetime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d+)"""",
    """"Act":"({action}[^"]+)""",
    """request=({result}\S+)\s""",
    """"Rcpt":"({email_recipients}({dest_email_address}[^\s@;,"]+@[^\s@;,"]+)[^"]*)"""",
    """"Subject":"(|({email_subject}[^"]+?))\s*"""",
    """"Dir":"({direction}[^"]+?)"""",
    """"IP":"({src_ip}[A-Fa-f\d:.]+)"""",
    """"aCode":"(|({alert_id}[^"]+?))"""",
    """"Sender":"(<>|({email_address}[^"]+))"""",
    """"MsgId":"<({message_id}[^"]+?)>""""
    """"Virus":"({alert_name}[^"]+)""""
  ]


}
```
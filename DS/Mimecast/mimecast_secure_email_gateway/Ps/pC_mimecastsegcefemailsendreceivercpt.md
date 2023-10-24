#### Parser Content
```Java
{
Name = mimecast-seg-cef-email-send-receive-rcpt
  ParserVersion = v1.0.0
  Vendor = Mimecast
  Product = Mimecast Secure Email Gateway
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ 
""""acc":""""
""""MsgId":""""
""""Cphr":""""
""""aCode":"""" 
""""Dir":""""
""""Sender":""""
""""Rcpt":""""
]
  Fields = [
    """"acc":"({host}[^",]+)"""",
    """"datetime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d+)"""",
    """"Act":"({action}[^"]+)""",
    """request=({result}\S+)\s""",
    """"Rcpt":"({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)[^"]*)"""",
    """"Subject":"(|({email_subject}[^"]+?))\s*"""",
    """"Dir":"({direction}[^"]+?)"""",
    """"IP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"aCode":"(|({alert_id}[^"]+?))"""",
    """"Sender":"(<>|({src_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""",
    """"MsgId":"<({message_id}[^"]+?)>""""
    """"Virus":"({alert_name}[^"]+)""""
    """"Err":"({failure_reason}[^"]+)""""
  ]


}
```
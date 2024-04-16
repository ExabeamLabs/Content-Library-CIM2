#### Parser Content
```Java
{
Name = mimecast-seg-sk4-email-send-receive-defaulttenant
  Vendor = Mimecast
  Product = Mimecast Secure Email Gateway
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"acc":""", """"Delivered":""", """"Dir":"""", """"MsgId":"""", """"Subject":"""", """"Sender":"""", """"aCode":"""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) ([\w.\-]+) """,
    """"aCode":"(|({alert_id}[^"]+?))"""",
    """"Dir":"({direction}[^"]+?)"""",
    """"Subject":"(|({email_subject}[^"]+?))([\\]+)?\s*"""",
    """dproc=({dproc}[^=]+)\s\w+=""",
    """request=({result}[^\s]+)""",
    """requestClientApplication=({user_agent}.+?)\s\w+=""",
    """suser=({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """"Rcpt":"({recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^"]*)"""",
    """"Rcpt":"({external_address}[^\s@;,]+@[^\s@;,"]+)""" 
    """senders:\s*({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    """"Error":"({failure_reason}[^"]+)"""
  ]
  ParserVersion = v1.0.0


}
```
#### Parser Content
```Java
{
Name = mimecast-seg-sk4-email-send-receive-defaulttenant
  Vendor = Mimecast
  Product = Mimecast Secure Email Gateway
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSZ" , "yyyy-MM-dd'T'HH:mm:ssZ" ]
  Conditions = [ """"acc":""", """"Delivered":""", """"Dir":"""", """"MsgId":"""", """"Subject":"""", """"Sender":"""", """"aCode":"""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) ([\w.\-]+) """,
    """"aCode":"(|({alert_id}[^"]+?))"""",
    """"Dir":"({direction}[^"]+?)"""",
    """"Subject":"(|({email_subject}[^"]+?))([\\]+)?\s*"""",
    """dproc=({dproc}[^=]+)\s\w+=""",
    """request=({result}[^\s]+)""",
    """requestClientApplication=({user_agent}.+?)\s\w+=""",
    """suser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """"Rcpt":"({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^"]*)"""",
    """"(?i)Sender":\s*"(<>|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))""""
    """"Error":"({failure_reason}[^"]+)"""
    """"Delivered":"({result}[^"]+)""""
    """"datetime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d+)""""
    """"MsgId":"<({message_id}[^"]+?)>"""",
  ]
  ParserVersion = v1.0.0


}
```
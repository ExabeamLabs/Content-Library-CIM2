#### Parser Content
```Java
{
Name = mimecast-seg-sk4-email-send-receive-acode
  Vendor = Mimecast
  Product = Mimecast Secure Email Gateway
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSZ" , "yyyy-MM-dd'T'HH:mm:ssZ" ]
  Conditions = [ """"Dir":""", """"aCode":""", """"acc":"""", """"Sender":"""",  """"Rcpt":""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) ([\w.\-]+) """,
    """"aCode":"(|({alert_id}[^"]+?))"""",
    """"Dir":"({direction}[^"]+?)"""",
    """dproc=({dproc}[^=]+)\s\w+=""",
    """requestClientApplication=({user_agent}.+?)\s\w+=""",
    """"Rcpt":"({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^"]*)"""",
    """"Sender":"(<>|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""",
    """"headerFrom":"(<>|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""",
    """"datetime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d+)"""",
    """"MsgId":"<({message_id}[^"]+?)>"""",
    """"SpamScore":\s*"?({spam_score}\d+)""",
    """"Subject":"({email_subject}[^"]+)"""",
    """"Act":"({action}[^"]+)""""

  ]
  ParserVersion = v1.0.0


}
```
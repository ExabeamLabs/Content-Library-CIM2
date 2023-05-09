#### Parser Content
```Java
{
Name = mimecast-seg-sk4-email-send-receive-defaulttenant
  Vendor = Mimecast
  Product = Mimecast Secure Email Gateway
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """CEF:""", """destinationServiceName =Mimecast Email Security""", """dtz=default-tenant""", """request=""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) ([\w.\-]+) """,
    """"acc":"({user}[^"]+)""",
    """"aCode":"(|({alert_id}[^"]+?))"""",
    """"Dir":"({direction}[^"]+?)"""",
    """"Subject":"(|({email_subject}[^"]+?))([\\]+)?\s*"""",
    """dproc=({dproc}[^=]+)\s\w+=""",
    """request=({result}[^\s]+)""",
    """requestClientApplication=({user_agent}.+?)\s\w+=""",
    """suser=({src_email_address}[^\s]+)""",
    """"Rcpt":"({recipients}({dest_email_address}[^\s@;,"]+@[^\s@;,"]+)[^"]*)"""",
    """"Rcpt":"({external_address}[^\s@;,]+@[^\s@;,"]+)""" 
  ]
  ParserVersion = v1.0.0


}
```
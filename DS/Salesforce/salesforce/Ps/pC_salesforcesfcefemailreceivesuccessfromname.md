#### Parser Content
```Java
{
Name = salesforce-sf-cef-email-receive-success-fromname
  ParserVersion = v1.0.0
  Vendor = Salesforce
  Product = Salesforce
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
    """ToAddress\=""",
    """Subject\=""",
    """type\=EmailMessage""",
    """FromName\=""",
    """FromAddress\=""",
    """destinationServiceName =Sales Cloud"""
  ]
  Fields = [
    """\Wsuser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """\Wcs2=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s+(\w+=|$)""",
    """ToAddress\\=({dest_email_address}.+?)(;\w+\\=|\s+\w+=|\s*$)""",
    """CcAddress\\=(?:null|({cc_address}.+?))(;\w+\\=|\s+\w+=|\s*$)""",
    """\Wcs2=.*?"user-email":"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """Subject\\=({email_subject}[^;]+?)(\s*\[\s*ref:.*?\])?\s*(;|\s+\w+=|\s+$)""",
    """ToAddress\\=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """LastModifiedDate\\=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z?)""",
    """\Wact=({alert_name}.+?)\s+(\w+=|$)""",
    """;Id\\=({alert_id}[^;\s]+)""",
    """({direction}o)"""
    """ValidatedFromAddress\\=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+));"""
  ]
  DupFields = [ "email_address->orig_user", "alert_name->alert_type", "dest_email_address->email_recipients" ]


}
```
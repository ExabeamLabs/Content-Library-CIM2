#### Parser Content
```Java
{
Name = microsoft-o365-cef-email-receive-success-fromname
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [
    """ToAddress\=""",
    """Subject\=""",
    """type\=EmailMessage""",
    """FromName\=""",
    """FromAddress\="""
  ]
  Fields = [
    """\Wsuser=({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """\Wcs2=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s+(\w+=|$)""",
    """ToAddress\\=({to_address}.+?)(;\w+\\=|\s+\w+=|\s*$)""",
    """CcAddress\\=(?:null|({cc_address}.+?))(;\w+\\=|\s+\w+=|\s*$)""",
    """\Wcs2=.*?"user-email":"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """Subject\\=({email_subject}[^;]+?)(\s*\[\s*ref:.*?\])?\s*(;|\s+\w+=|\s+$)""",
    """ToAddress\\=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """LastModifiedDate\\=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+)""",
    """\Wact=({alert_name}.+?)\s+(\w+=|$)""",
    """;Id\\=({alert_id}[^;\s]+)""",
    """({direction}o)"""
    """ValidatedFromAddress\\=({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+));"""
  ]
  DupFields = [ "src_email_address->orig_user", "alert_name->alert_type", "to_address->email_recipients" ]
 

}
```
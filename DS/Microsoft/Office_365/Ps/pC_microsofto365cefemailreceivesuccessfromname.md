#### Parser Content
```Java
{
Name = microsoft-o365-cef-email-receive-success-fromname
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Office 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [
    """ToAddress\=""",
    """Subject\=""",
    """type\=EmailMessage""",
    """FromName\=""",
    """FromAddress\="""
  ]
  Fields = [
    """\Wsuser=({email_address}[^@]+@[^@\s]+)""",
    """\Wcs2=({dest_email_address}[^@]*@[^@=]+?)\s+(\w+=|$)""",
    """ToAddress\\=({to_address}.+?)(;\w+\\=|\s+\w+=|\s*$)""",
    """CcAddress\\=(?:null|({cc_address}.+?))(;\w+\\=|\s+\w+=|\s*$)""",
    """\Wcs2=.*?"user-email":"({dest_email_address}[^@"]+@[^"]+)""",
    """Subject\\=({email_subject}[^;]+?)(\s*\[\s*ref:.*?\])?\s*(;|\s+\w+=|\s+$)""",
    """LastModifiedDate\\=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+)""",
    """\Wact=({alert_name}.+?)\s+(\w+=|$)""",
    """Id\\=({alert_id}[^;\s]+)""",
    """({direction}o)"""
  ]
  DupFields = [ "email_address->orig_user", "alert_name->alert_type", "to_address->email_recipients" ]
 

}
```
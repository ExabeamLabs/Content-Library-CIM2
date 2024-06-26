#### Parser Content
```Java
{
Name = salesforce-sf-cef-email-send-success-emailmessage
  ParserVersion = v1.0.0
  Vendor = Salesforce
  Product = Salesforce
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
    """destinationServiceName =Sales Cloud""",
    """type\\=EmailMessage"""
  ]
  Fields = [
    """LastModifiedDate\\=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)""",
    """ValidatedFromAddress\\=({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+));""",
    """Subject\\=({email_subject}[^;=]+);\w+\\=""",
    """ToAddress\\=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """ToAddress\\=({email_recipients}[^=]+?)\s+("|$)""",
    """CcAddress\\=(?:null|({cc_address}[^;]+?))(;\w+\\=|\s+\w+=|\s*$)"""
  ]
  DupFields = [ "src_email_address->orig_user", "email_recipients->to_address" ]


}
```
#### Parser Content
```Java
{
Name = symantec-esc-cef-alert-trigger-success-emailseccloud
  ParserVersion = v1.0.0
  Vendor = Symantec
  Product = Symantec Email Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """destinationServiceName =Symantec Email Security.cloud""", """CEF""", """|security-threat-detected|"""]
  Fields = [
    """"severity"+:"+({alert_severity}[^"]+)"""",
    """cat=({alert_type}[^\s]+)\s""",
    """destinationServiceName =({service_name}.+?)\s*\w+=""",
    """dpriv=({alert_type}.+?)\s*\w+=""",
    """dproc=(N\/A|({process_name}.+?))\s*\w+=""",
    """msg=({alert_name}.+?)\s*\w+=""",
    """requestContext=({target}.+?)\s*\w+=""",
    """requestClientApplication=({app}.+?)\s*\w+=""",
    """"headerTo":\[({email_recipients}[^\]]+)\],""",
    """"headerTo":\["({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """"subject":"({email_subject}[^"]+)",""",
    """"messageSize":({bytes}\d+)""",
  ]
  DupFields = [ "dest_email_address->external_address" ]


}
```
#### Parser Content
```Java
{
Name = netskope-sc-cef-app-logout-logoutsuccessful
  ParserVersion = v1.0.0
  Vendor = Netskope
  Product = Netskope Security Cloud
  TimeFormat = "epoch_sec"
  Conditions = [ """audit_log_event":""", """"Logout Successful""", """"type":""", """destinationServiceName =Netskope""" ]
  Fields = [
    """"timestamp":({time}\d{10})""",
    """requestClientApplication=({app}.+?)\s+(\w+=|$)""",
    """"category":\s*"({additional_info}[^"]+)""",
    """"user":\s*"(unknown|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))""",
    """"audit_log_event":\s*"({operation}[^"]+)""",
  ]


}
```
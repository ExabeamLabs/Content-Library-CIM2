#### Parser Content
```Java
{
Name = tyco-ccure-json-app-logout-success-operatorlogin
  Vendor = Tyco
  Product = CCURE Building Management System
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"messagetype":"OperatorLogin"""", """"statecode":"LoggedOut"""", """"primaryobjectname":"""" ]
  Fields = [
    """"messageutc":"({time}[^"]+)""",
    """"statecode":"({event_name}[^"]+)""",
    """"primaryobjectname":"({last_name}[^",]+?)\s*,\s*({first_name}[^",]+?)\s*"""",
    """<ApplicationName[^>]*>({app}[^<"]+)<\/ApplicationName>""",
  ]


}
```
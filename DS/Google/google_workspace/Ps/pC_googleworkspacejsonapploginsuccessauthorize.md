#### Parser Content
```Java
{
Name = google-workspace-json-app-login-success-authorize
  ParserVersion = v1.0.0
  Vendor = Google
  Product = Google Workspace
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"applicationName":""", """"token"""", """"uniqueQualifier":""",  """"authorize"""" ]
  Fields = [
    """"time"\s*:\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"profileId"\s*:\s*"({user_id}\d+)""",
    """suser=(anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+[\w=]+""",
    """"actor"\s*:\s*\{[^=]*?"email"\s*:\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """"name"\s*:\s*"client_id",\s*"value"\s*:\s*"({account}[^"]+)"""",
    """"name"\s*:\s*"app_name",\s*"value"\s*:\s*"({app}[^"]+)"""",
  ]


}
```
#### Parser Content
```Java
{
Name = airlock-allowlisting-json-app-activity-success-serveractivity
  Vendor = Airlock
  Product = Airlock Allowlisting
  TimeFormat = "dd/MM/yyyy HH:mm:ss a"
  Conditions = [ """"event":"ServerActivityMessage"""", """"user":"""", """"datetime":"""", """"task":"""" ]
  Fields = [
    """"datetime":"({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s\w{2})"""",
    """"user":"(SYSTEM|LOCAL SERVICE|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|({user}[\w\.\-]{1,40}\$?)))"""",
    """({event_name}ServerActivityMessage)""",
    """"task":"({operation}[^"]+)""",
    """"description":"({additional_info}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```
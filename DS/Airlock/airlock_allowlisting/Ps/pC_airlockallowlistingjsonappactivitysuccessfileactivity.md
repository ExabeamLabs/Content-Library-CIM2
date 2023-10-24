#### Parser Content
```Java
{
Name = airlock-allowlisting-json-app-activity-success-fileactivity
  Vendor = Airlock
  Product = Airlock Allowlisting
  TimeFormat = "dd/MM/yyyy HH:mm:ss a"
  Conditions = [ """"event":"FileActivityMessage"""", """"username":"""", """"datetime":"""",  ]
  Fields = [
    """"datetime":"({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s\w{2})"""",
    """"hostname":"({host}[\w\-\.]+)""",
    """"username":"(SYSTEM|LOCAL SERVICE|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)))"""",
    """"path":"({file_dir}[^"]+)""",
    """filename":"({file_name}[^"]+?(\.(\d{1,5}|({file_ext}[^\."]+)))?)""""
    """({event_name}FileActivityMessage)""",
    """"sha256":"({hash_sha256}[^"]+)""""
    """"md5":"({hash_md5}[^"]+)""",
    """"parentprocess":"({process_name}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```
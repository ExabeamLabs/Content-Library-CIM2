#### Parser Content
```Java
{
Name = fireeye-endpointsecurity-json-alert-trigger-success-fireeyehx
  Vendor = FireEye
  Product = FireEye Endpoint Security (HX)
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"FireEyeHX"""", """"HX"""", """"malwarePath":"""", """"malwareMD5":"""" ]
  Fields = [
    """"@timestamp":"({time}\d\d\d\d\-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """"deviceIP":"({host}[A-Fa-f:\d.]+)""",
    """"deviceHostname":"({host}[\w\-.]+)""",
    """"srcIP":"({src_ip}[A-Fa-f:\d.]+)""",
    """"malwarePath":"({malware_url}[^"]+)""",
    """"userID":"(({domain}[^"\\\s]+)\\+)?({user}[^"\\\s]+)""",
    """"srcOS":"({os}[^"]+)""",
    """"process":\s*"({alert_name}[^"]+)""",
    """"log_type":"({alert_type}[^"]+)""",
    """"srcHostname":"({src_host}[\w\-.]+)""",
    """"malwareMD5":"({hash_md5}[^"]+)""",
    """"deviceSensor":"({sensor}[^"]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```
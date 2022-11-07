#### Parser Content
```Java
{
Name = unix-unixnamed-json-app-notification-insecurity
  Conditions = [ """"message":"insecurity proof failed resolving""" ]
  ParserVersion = "v1.0.0"

bind-events = {
  Vendor = Unix
  Product = Unix Named
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"@timestamp":"({time}[^"]+)""",
    """"severity":({severity}[^",]+)""",
    """"priority":({priority}[^",]+)""",
    """"hostname":"({host}[^",]+)""",
    """"source":"({log_source}[^",]+)""",
    """"source":"[^"]*?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """"message":"[^"]*?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\#({src_port}\d+)""",
    """"message":"({additional_info}[^"]+?)\s*"""",
  
}
```
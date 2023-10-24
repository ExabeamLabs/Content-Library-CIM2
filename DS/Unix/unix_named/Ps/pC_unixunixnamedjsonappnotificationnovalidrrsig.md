#### Parser Content
```Java
{
Name = unix-unixnamed-json-app-notification-novalidrrsig
  Conditions = [ """"message":"no valid RRSIG resolving""" ]
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
    """"source":"[^"]*?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(.log)(:({src_port}\d+))?""",
    """"message":"[^"]*?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\#|:)?({src_port}\d+)?""",
    """"message":"({additional_info}[^"]+?)\s*"""",
  
}
```
#### Parser Content
```Java
{
Name = mcafee-es-kv-endpoint-notification-windowserror
  ParserVersion = "v1.0.0" 
  Vendor = McAfee
  Product = McAfee Endpoint Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ "McAfee ", "Windows error event", "ERROR" ]
  Fields = [
    """"@timestamp"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"host"*:"*({host}[^"]+)""",
    """"groups"*:\[({groups}[^\]]+)""",
    """"dstuser"*:"*\(?(no user|({user}[^"\)]+))""",
    """"status"*:"*({result}[^"]+)""",
    """"data"*:\{[^\{\}]*?"id"*:"*({error_code}[^"]+)"*""",
    """"system_name"*:"*({dest_host}[^"]+)""",
    """"decoder"*:\{[^\{\}]*?"name":"({decoder_name}[^"]+)""",
# full_log is removed
    """"full_log"*:"*.+? ERROR\(({error_code}[^\)]+)""",
    """"full_log"*:"*[^"]*?attempt to modify file '({target}[^"']+)' by process ({process_path}({process_dir}(?:(\w+:)*([\\\/]+[^\\\/']+)+)?[\\\/]+)({process_name}.+?))\s+\(""",
    """"full_log"*:"*[^"]*?to (access|exploit) ({target}[^\s,]+)""",
  ]


}
```
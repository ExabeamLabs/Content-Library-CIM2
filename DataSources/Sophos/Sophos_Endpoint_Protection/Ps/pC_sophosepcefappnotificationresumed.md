#### Parser Content
```Java
{
Name = sophos-ep-cef-app-notification-resumed
  Product = Sophos Endpoint Protection
  ParserVersion = "v1.0.0"
  Conditions = ["""destinationServiceName =Sophos Central""",""""type":"Event::Endpoint::Management::Resumed"""" ]

sophos-events = {
  Vendor = Sophos
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"location":"({host}[^"]+)""",
    """"when":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"rt":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"name":\s*"({event_name}[^"]+)""",
    """"type":\s*"({event_category}[^"]+)""",
    """"dhost":\s*"({dest_host}[\w\-.]+)"""",
    """"severity":\s*"({severity}[^"]+)""",
    """"suser":\s*"(?:n\/a|({user}[^"\\\s,]+))"""",
    """"suser":\s*"(n\/a|({full_name}[^"\\\s,]+\s+[^"\\,]+))"""",
    """"suser":\s*"(n\/a|({last_name}[^",\\\s]+),\s*({first_name}[^,"\\\s]+))""",
    """"suser":\s*"(?:n\/a|({user}[^"\s]+))"""",
# id is removed
    """"source":"(?:n\/a|({user}[^"\\\s]+))"""",
    """\\"source_info\\"__ip=({src_ip}[A-Fa-f:\d.]+)""",
    """"source_info":\s*\{"ip":\s*"({src_ip}[A-Fa-f:\d.]+)""",
    """"source":"(({domain}[^\\",]+?)\\+)?(?:n\/a|Administrator|({full_name}(?:({first_name}[^\s",.\\]+)(?:\s+|\.))({last_name}[^",\\]+)))"""",
    """"source":"((({domain}[^\",]+?)\\+)?(?:n/a|Administrator|({user}[^"\s]+)))"""",
    """destinationServiceName =({app}[^=]+)\s+\w+="""
  ]
  DupFields = [ "host->src_host" 
}
```
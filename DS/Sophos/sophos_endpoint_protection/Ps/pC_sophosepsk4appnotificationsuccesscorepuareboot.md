#### Parser Content
```Java
{
Name = sophos-ep-sk4-app-notification-success-corepuareboot
  ParserVersion = "v1.0.0"
  Product = Sophos Endpoint Protection
  Conditions = [ """"Event::Endpoint::CorePuaReboot"""" ]

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
    """\\"source_info\\"__ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"source_info":\s*\{"ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"source":"(({domain}[^\\",]+?)\\+)?(?:n\/a|Administrator|({full_name}(?:({first_name}[^\s",.\\]+)(?:\s+|\.))({last_name}[^",\\]+)))"""",
    """"source":"((({domain}[^\",]+?)\\+)?(?:n/a|Administrator|({user}[^"\s]+)))"""",
    """destinationServiceName =({app}[^=]+)\s+\w+="""
  ]
  DupFields = [ "host->src_host" 
}
```
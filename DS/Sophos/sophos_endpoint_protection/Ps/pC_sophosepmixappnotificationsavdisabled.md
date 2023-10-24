#### Parser Content
```Java
{
Name = sophos-ep-mix-app-notification-savdisabled
  Product = Sophos Endpoint Protection
  ParserVersion = "v1.0.0"
  Conditions = [ """Event::Endpoint::SavDisabled""" ]

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
    """"suser":\s*"(?:n\/a|({user}[\w\.\-]{1,40}\$?))"""",
    """"suser":\s*"(n\/a|({full_name}[^"\\\s,]+\s+[^"\\,]+))"""",
    """"suser":\s*"(n\/a|({last_name}[^",\\\s]+),\s*({first_name}[^,"\\\s]+))""",
    """"suser":\s*"(?:n\/a|({user}[\w\.\-]{1,40}\$?))"""",
# id is removed
    """"source":"(?:n\/a|({user}[\w\.\-]{1,40}\$?))"""",
    """\\"source_info\\"__ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"source_info":\s*\{"ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"source":"(({domain}[^\\",]+?)\\+)?(?:n\/a|Administrator|({full_name}(?:({first_name}[^\s",.\\]+)(?:\s+|\.))({last_name}[^",\\]+)))"""",
    """"source":"((({domain}[^\",]+?)\\+)?(?:n/a|Administrator|({user}[\w\.\-]{1,40}\$?)))"""",
    """destinationServiceName =({app}[^=]+)\s+\w+="""
  ]
  DupFields = [ "host->src_host" 
}
```
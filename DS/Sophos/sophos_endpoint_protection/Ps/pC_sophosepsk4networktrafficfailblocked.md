#### Parser Content
```Java
{
Name = sophos-ep-sk4-network-traffic-fail-blocked
  ParserVersion = v1.0.0
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """CEF:""", """"type":"Event::Endpoint::WindowsFirewall::Blocked"""" ]
  Fields = [
    """"location":"({host}[\w\-.]+)"""",
    """Event::Endpoint::WindowsFirewall::({action}Blocked)""",
    """"when":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"name":"({additional_info}[^"]+)""""
    """"source_info":\s*\{[^\}]*?"ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"type":"({event_name}[^"]+)"""",
    """"source":"(({full_name}[^\s",]+[\s,]{1,100}[^\s",]+)|({user}[^",\s]+))""""
    """"source":"(n\/a|(([^\\\s"]*\s{1,100}[^\\"]*|(DOMAIN|({domain}[^\\"]+)))\\+)?({user}[^\\\s"]+))"""",

  ]
  DupFields = ["host->src_host"]


}
```
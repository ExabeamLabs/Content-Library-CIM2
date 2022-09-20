#### Parser Content
```Java
{
Name = sophos-ep-cef-app-notification-registered
  ParserVersion = v1.0.0
  Product = Sophos Endpoint Protection
  Conditions = [ """CEF:""", """"Event::Endpoint::Registered""" ]

cef-sophos-dlp-alert-1 = {
  Vendor = Sophos
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"location":"({host}[\w\-.]+)"""",
    """"when":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"type":"({alert_type}Event[^"]+)""",
    """"description":"({alert_name}[^"]+?)\.?"""",
    """"name":"({alert_name}[^"]+)""",
    """"group":"({additional_info}[^"]+)""",
    """"name":\s*"(n\/a|({alert_name}[^\:\"\']+(\:\s*\'({target}[^\"\']+))?\'))""",
    """"name":\s*"(n\/a|[^"]*? at \'({additional_info}({malware_url}[^"\']+)))""",
    """"severity":"({alert_severity}[^"]+)""",
    """"id":"({alert_id}[^"]+)""",
    """"location":"({src_host}[^"]+)""",
    """"source":"(n\/a|({full_name}[^"\\\(\),]+))"""",
    """"source":"(n\/a|({last_name}[^",\s]+),\s*({first_name}[^,"\s]+))""",
    """"source":"(n\/a|(([^\\\s"]*\s+[^\\"]*|({domain}[^\\"]+))\\+)?(?:Administrator|({user}[^\\\s"]+)))"""",
    """"source":"(n\/a|([\w\-.]+)\s*(\(({src_ip}[A-Fa-f:\d.]+)\))?)"""",
    """"ip":"({src_ip}[A-Fa-f:\d.]+)""""
  
}
```
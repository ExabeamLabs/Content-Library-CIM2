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
    """"source":"(n\/a|([\w\-.]+)\s*(\(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\))?)"""",
    """"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  
}
```
#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-dns-dnsclient"
  Conditions = [ """<EventID>""", """Microsoft-Windows-DNS-Client""", """<Channel>""" ]
  ParserVersion = "v1.0.0"

xml-dns-events}{
  Name = "microsoft-evsecurity-xml-dns-dnsclient"
  Conditions = [ """<EventID>""", """Microsoft-Windows-DNS-Client""", """<Channel>""" ]
  ParserVersion = "v1.0.0"
}

{
 Name = ibm-datapower-str-app-activity-fail-auditerror
 Vendor = IBM
 Product = IBM Datapower
 ParserVersion = "v1.0.0"
 TimeFormat = "MMM dd HH:mm:ss"
 Conditions = [ """[audit][error]""", """trans(""" ]
 Fields = [
   """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)\s+({host}[\w-.]+)\s+\[({event_code}[^\]\s]+)\]\[({event_category}[^\]]+)\]\[({severity}[^\]]+)\]\s+trans\(\d+\)[^:]*:\s\(({user}[\w\.\-\!\#\^\~]{1,40}\$?):({domain}[^:]+):(\*|({object}[^:]+)):(\*|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\):\s+({additional_info}[\s\S]+?)$""",
   """:\s({object_type}[^\s]+)\s'({service_name}[^']+)'\s*-\s*({description}Request from\s*(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+)))?\s*to\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s*({action}\w+)($|\s*by the processing policy|policy))"""
   """:\s({object_type}[^\s]+)\s'({service_name}[^']+)'\s*-\s*({description}Operation state transition to up\s*({action}\w+))"""
   """:\s({object_type}[^\s]+)\s'({service_name}[^']+)'\s*-\s*({description}QM\s*({action}\w+))"""
   """:\suser\s'({user}[\w\.\-\!\#\^\~]{1,40}\$?)'\s*-\s*({description}({event_name}({action}\w+)\s*authentication))"""
   
}
```
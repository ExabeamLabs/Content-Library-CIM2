#### Parser Content
```Java
{
Name = sophos-ep-cef-app-notification-success-notprotected
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """"type":"Event::Endpoint::NotProtected"""" ]

cef-sophos-security-alert-1-dl = {
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"when":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"location":"({host}[\w\-.]+)"""",
    """"id":"({alert_id}[^"]+)""",
    """"severity":"({alert_severity}[^"]+)""",
    """"name":\s*"(n\/a|({alert_name}[^\:\"\']+(\:\s*\'({target}[^\"\']+))?\'))""",
    """"name":\s*"(n\/a|[^"]*? at \'({additional_info}({malware_url}[^"\']+)))""",
    """"name":\s*"(n\/a|[^"]*? at \'({additional_info}({process_path}[^']+\\({process_name}[^']+))))""",
    """"type":"({alert_name}Event::Endpoint::[^"]+)""",
    """"name":"({alert_name}[^":]+?)\s*(:\s*({app}[^":,\\]+))?"""",
    """"threat":"?(null|({alert_name}[^",:]+))""",
    """"type":"({alert_type}Event::Endpoint::[^"]+)""",
    """"source":"(n\/a|({full_name}[^"\\\(\),]+))",""",
    """"source":"(n\/a|(([^\\\s"]*\s+[^\\"]*|({domain}[^\\"]+?))\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"source":"(n\/a|([\w\-.]+)\s*(\(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\))?)"""",
    """"description":"({additional_info}[^:"]+:?([^"]+? at '({malware_url}[^"]+)')?)"""",
    """"descriptor":"({process_path}[^\s]+\\({process_name}[^"]+))"""",
  ]
  DupFields = ["host->src_host"
}
```
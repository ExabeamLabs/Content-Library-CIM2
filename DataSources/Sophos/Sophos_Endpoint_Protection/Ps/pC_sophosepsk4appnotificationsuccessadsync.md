#### Parser Content
```Java
{
Name = sophos-ep-sk4-app-notification-success-adsync
  Conditions = [ """CEF:""", """destinationServiceName =Sophos Central""", """"type":"Event::ADSync::Success"""", """"group":"AD_SYNC"""", """"severity":"""" ]
   Fields=${SophosParsersTemplates.cef-sophos-security-alert-1.Fields}[
    """"type":"({alert_name}[^"]+)"""",
    """"group":"({alert_type}[^"]+)"""",
    """"name":"({additional_info}[^"]+)""""
  ]
  DupFields = [ "alert_name->event_name"]
  ParserVersion = "v1.0.0"

cef-sophos-security-alert-1 = {
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
    """"source":"(n\/a|({full_name}[^"\\\(\),]+))"""",
    """"source":"(n\/a|({last_name}[^",\\\s]+),\s*({first_name}[^,"\s\\]+))""",
    """"source":"(n\/a|(([^\\\s"]*\s+[^\\"]*|({domain}[^\\"]+?))\\+)?({user}[^\\\s"]+))"""",
    """"ip":"({src_ip}[A-Fa-f:\d.]+)""""
    """"source":"(n\/a|([\w\-.]+)\s*(\(({src_ip}[A-Fa-f:\d.]+)\))?)"""",
    """"description":"({additional_info}[^:"]+:?([^"]+? at '({malware_url}[^"]+)')?)"""",
    """"descriptor":"({process_path}[^\s]+\\({process_name}[^"]+))"""",
  ]
  DupFields = ["host->src_host"
}
```
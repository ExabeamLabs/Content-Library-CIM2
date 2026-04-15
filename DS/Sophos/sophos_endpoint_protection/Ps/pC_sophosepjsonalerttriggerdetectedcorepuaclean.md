#### Parser Content
```Java
{
Name = sophos-ep-json-alert-trigger-detected-corepuaclean
  ParserVersion = "v1.0.0"
  Conditions = [ """"type":"Event::Endpoint::CorePuaClean"""", """"endpoint_id":""", """"endpoint_type":""" ]

sophos-security-alert-1 {
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"when":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"location":"({src_host}({host}((\d{1,3}\.){3}\d{1,3}|({=src_host}[\w\-.]+))))"""",
    """"id":"({alert_id}[^"]+)""",
    """"severity":"({alert_severity}[^"]+)""",
    """"name":\s*"(n\/a|({event_name}({alert_name}[^\:\"\']+(\:\s*\'({target}[^\"\']+))?\')))""",
    """"name":\s*"(n\/a|[^"]*? at \'({additional_info}({malware_url}[^"\']+)))""",
    """"name":\s*"(n\/a|[^"]*? at \'({additional_info}({process_path}[^']+\\({process_name}[^']+))))""",
    """"type":"({event_name}({alert_name}Event::Endpoint::[^"]+))""",
    """"name":"({event_name}({alert_name}[^"]+))""",
    """"threat":"?(null|({event_name}({alert_name}[^",]+)))""",
    """"type":"({alert_type}Event::Endpoint::[^"]+)""",
    """"source":"(n\/a|(\d{1,3}\.){3}\d{1,3}|({full_name}[^"\\\(\)]+))","\w+""",
    """"source":"(n\/a|(([^\\\s"]*\s+[^\\"]*|({domain}[^\\"]+?))\\+)?((\d{1,3}\.){3}\d{1,3}|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""",
    """"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"source":"(n\/a|([\w\-.]+)\s*(\(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\))?)"""",
    """"description":"({additional_info}[^:"]+:?([^"]+? at '({malware_url}[^"]+)')?)"""",
    """"descriptor":"({process_path}[^"]+\\({process_name}[^"]+))"""",
    """"endpoint_platform":"({os}[^"]+)"""
  sophos-security-alert = {
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"(rt|when)":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"name":\s*"(n\/a|({alert_name}[^\:\"]+)(\:\s*({target}[^\"]+))?)"""",
    """"name":\s*"(n\/a|({additional_info}[^"]+))""",
    """"name":\s*"(n\/a|({alert_name}[^\:\"\']+(\:\s*\'({target}[^\"\']+))?\'))""",
    """"name":\s*"(n\/a|[^"]*? at \'({additional_info}({malware_url}[^"\']+)))""",
    """"type":\s*"(n\/a|({alert_type}[^"]+))""",
    """"dhost":\s*"({src_host}[^"]+)""",
    """"severity":\s*"({alert_severity}[^"]+)""",
    """"(suser|source)":\s*"(n\/a|({full_name}[^"\\\(\),]+))"""",
    """"(suser|source)":\s*"(n\/a|({last_name}[^",\s]+),\s*({first_name}[^,"\s]+))""",
    """"(suser|source)":\s*"(n\/a|(({domain}[^\\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"(suser|source)":\s*"(n\/a|({src_host}[\w\-.]+)\s*(\(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\))?)"""",
    """"id":\s*"({alert_id}[^"]+)""",
    """filePath":\s"({process_path}[^"]+\\+({process_name}[^"]+))""",
  ]
}
}
```
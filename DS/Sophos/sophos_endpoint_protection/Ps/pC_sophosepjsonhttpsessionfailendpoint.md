#### Parser Content
```Java
{
Name = "sophos-ep-json-http-session-fail-endpoint"
ParserVersion = "v1.0.0"
Vendor = "Sophos"
Product = "Sophos Endpoint Protection"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""Event::Endpoint::Web"""
]
Fields = [

    """"location":"({host}[^"]+)""",
    """"(rt|when)":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"name":\s*"(n\/a|({alert_name}[^\:\"\']+(\:\s*\'({target}[^\"\']+))?\'))""",
    """"name":\s*"'({target}[^']+)'\s+({alert_name}[^"']+)\s""",
    """"name":\s*"({alert_name}[^"']+)\sto '({target}[^']+)'\s+""",
    """"name":\s*"'({malware_url}[^"\'\s]+)'\s+blocked due to""",
    """"name":\s*"[^"]*?block to\s+'({malware_url}[^"\'\s]+)'""",
    """"name":\s*"(n\/a|[^"]*? at \'({additional_info}({malware_url}[^"\']+)))""",
    """"name":\s*"({additional_info}[^}]+?)("\}|","\w+":)""",
    """"type":\s*"({alert_type}[^"]+)""",
    """"dhost":\s*"({src_host}[^"]+)""",
    """"severity":\s*"({alert_severity}[^"]+)""",
    """"(suser|source)":\s*"(n\/a|(({domain}[^\\"]+)\\+)?({full_name}[^\\\(\)\s",]+\s+[^\\\(\)",]+))"""",
    """"(suser|source)":\s*"(n\/a|({last_name}[^",\s]+),\s*({first_name}[^,"\s]+))""",
    """"(suser|source)":\s*"(n\/a|(({domain}[^\\"]+)\\+)?({user}[^\\\s"]+))"""",
    """"(suser|source)":\s*"(n\/a|([\w\-.]+)\s*(\(({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\))?)"""",
    """"id":\s*"({alert_id}[^"]+)""",
   ]


}
```
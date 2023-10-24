#### Parser Content
```Java
{
Name = sophos-ep-json-alert-trigger-success-webcontrolviolation
Vendor = "Sophos"
Product = "Sophos Endpoint Protection"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""Event::Endpoint::WebControlViolation""""
""""User bypassed category block """
]
Fields = [
""""rt":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
""""name":\s*"({alert_name}[^'"]+) to '({malware_url}[^'"]+)"""
""""name":\s*"({additional_info}[^"]+)"""
""""type":\s*"({alert_type}[^"]+)"""
""""dhost":\s*"({src_host}[^"]+)"""
""""severity":\s*"({alert_severity}[^"]+)"""
""""(suser|source)":\s*"(n\/a|(({domain}[^\\"]+)\\+)?({full_name}[^\\\(\)\s",]+\s+[^\\\(\)",]+))""""
""""(suser|source)":\s*"(n\/a|({last_name}[^",\\\s]+),\s*({first_name}[^,"\\\s]+))"""
""""(suser|source)":\s*"(?:n\/a|({user}[\w\.\-]{1,40}\$?))""""
""""(suser|source)":\s*"(({domain}[^\\",]+)\\+)?({user}[\w\.\-]{1,40}\$?)""""
""""id":\s*"({alert_id}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```
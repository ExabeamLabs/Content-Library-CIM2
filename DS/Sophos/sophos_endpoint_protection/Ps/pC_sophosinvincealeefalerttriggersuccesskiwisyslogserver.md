#### Parser Content
```Java
{
Name = "sophos-invincea-leef-alert-trigger-success-kiwisyslogserver"
Vendor = "Sophos"
Product = "Sophos Endpoint Protection"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""LEEF:1.0|Invincea|"""
]
Fields = [
"""\s\d{1,2} \d\d:\d\d:\d\d\s+({host}[^\s]+)"""
"""devTime1=({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)"""
"""LEEF[^|]+?\|([^|]+\|){4}({alert_name}[^|]+)"""
"""sev=({alert_severity}\d+)"""
"""usrName =(?:|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+="""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\ssrcHostName =({src_host}[^\s]+)"""
"""\|externalId=({alert_id}\d+)"""
"""\surl=(?:|({malware_url}.+?))\s+\w+="""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```
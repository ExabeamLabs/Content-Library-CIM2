#### Parser Content
```Java
{
Name = "imperva-securesphere-kv-alert-trigger-success-alertinfo"
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = ["yyyy-MM-dd HH:mm:ss", "EEE MMM dd HH:mm:ss zzz yyyy"]
Conditions = [
"""SecSphWeb"""
""";AlertInformation="""
""";AlertType="""
]
Fields = [
"""\d\d:\d\d:\d\d ({host}\S+) SecSphWeb"""
"""AlertCreateTime=({time}\w+ \w+ \d+ \d\d:\d\d:\d\d \w+ \d\d\d\d)"""
"""AlertCreateTime=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""AlertInformation=({alert_name}[^;]+)"""
"""AlertType=({alert_type}[^;]+)"""
"""Severity=({alert_severity}[^;]+)"""
"""AlertDescription=({additional_info}[^;]+)"""
"""SourceIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""SourcePort=({src_port}\d+)"""
"""AttackedApp=({app}[^;]+)"""
"""DestinationIP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""DestinationPort=({dest_port}\d+)"""
"""EventNumber=({alert_id}\d+)"""
"""Alert\.username=(n\/a|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
]
ParserVersion = "v1.0.0"


}
```
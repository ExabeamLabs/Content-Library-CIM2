#### Parser Content
```Java
{
Name = "imperva-securesphere-leef-alert-trigger-success-alertdescription"
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = ["yyyy-MM-dd HH:mm:ss","EEE MMM dd HH:mm:ss zzz yyyy"]
Conditions = [
"""|Imperva|SecureSphere|"""
"""|Alert ID="""
"""|Alert type="""
"""|Alert Description="""
]
Fields = [
"""(\s|\|)devTime=({time}\w+ \w+ \d+ \d\d:\d\d:\d\d \w+ \d\d\d\d)"""
"""(\s|\|)devTime=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""(\s|\|)Alert ID=({alert_id}\d+)"""
"""(\s|\|)Alert type=({alert_type}[^\|]+)"""
"""(\s|\|)src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""(\s|\|)dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""(\s|\|)usrName ="*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""(\s|\|)Application name=({app}[^\|]+)"""
"""(\s|\|)Alert Description=({additional_info}[^\|]+)"""
"""(\s|\|)Severity=({alert_severity}[^\|]+)"""
"""(\s|\|)ServerGroupName =({server_group}[^\|]+)"""
]
DupFields = [
"alert_type->alert_name"
]
ParserVersion = "v1.0.0"


}
```
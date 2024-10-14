#### Parser Content
```Java
{
Name = "redcanary-rc-kv-alert-trigger-success-headline"
Vendor = "Red Canary"
Product = "Red Canary Managed Detection and Response"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""", u'headline':"""
""", u'subclassifications':"""
]
Fields = [
"""u'timestamp':\s*u'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
"""u'subclassifications':\s*\[u'({alert_type}[^'\]]+)"""
"""u'severity':\s*u'({alert_severity}[^'\]]+)"""
"""u'headline':\s*u'({alert_name}[^',]+)"""
"""u'url':\s*u'({malware_url}[^']+)"""
"""u'path':\s*u'({process_path}({process_dir}(?:[^']+)?[\\\/])?({process_name}[^\\\/']+))"""
"""u'md5':\s*u'({hash_md5}[^']+)"""
"""u'username':\s*u'({user}[\w\.\-\!\#\^\~]{1,40}\$?)'"""
"""u'sensor_id':\s*u'({sensor_id}[^']+)"""
"""u'ip_addresses':\s*\[u'({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""u'hostname':\s*u'({src_host}[^']+)"""
"""u'summary':\s*u'({additional_info}[^']+)"""
]
ParserVersion = "v1.0.0"


}
```
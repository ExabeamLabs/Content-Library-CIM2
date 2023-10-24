#### Parser Content
```Java
{
Name = "fireeye-endpointsecurity-json-alert-trigger-success-eventat"
Vendor = "FireEye"
Product = "FireEye Endpoint Security (HX)"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""hostname":"""
""""event_at":"""
""""infection-name":"""
""""detections":"""
""""infected-object":"""
]
Fields = [
"""event_at":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
"""infection-name":\s*"({alert_name}[^"]+)"""
"""hostname":\s*"({host}[^"]+)"""
"""last_poll_ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""infection-type":\s*"({alert_type}[^"]+)"""
""""alert_id":\s*({alert_id}\d+)"""
""""infection":\s*\{"confidence-level":\s*"({alert_severity}[^"]+)""""
""""applied-action":\s*"((?i)none|({action}[^"]+))"""
""""infected-object":[^}]+?file-path":\s*"({file_path}(({file_dir}[^"]*?[\\\/]+)?({file_name}[^\\\/"]+?(\.({file_ext}\w+))?)))""""
""""username":\s*"((?i)SYSTEM|({user}[\w\.\-]{1,40}\$?))""""
""""domain":\s*"((?i)NT AUTHORITY|({domain}[^"]+))""""
"""infected-object":[^}]+?md5sum":\s*"({hash_md5}[^"]+)"""
"""infected-object":[^}]+?sha1sum":\s*"({hash_sha1}[^"]+)"""
"""infected-object":[^}]+?sha256sum":\s*"({hash_sha256}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```
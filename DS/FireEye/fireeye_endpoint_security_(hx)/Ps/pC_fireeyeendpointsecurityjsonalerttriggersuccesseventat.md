#### Parser Content
```Java
{
Name = "fireeye-endpointsecurity-json-alert-trigger-success-eventat"
Vendor = "FireEye"
Product = "FireEye Endpoint Security (HX)"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
ExtractionType = json
Conditions = [
""""hostname":"""
""""event_at":"""
""""infection-name":"""
""""detections":"""
""""infected-object":"""
]
Fields = [
"""exa_json_path=$.event_at,exa_field_name=time""",
"""exa_json_path=$..infection.infection-name,exa_field_name=alert_name""",
"""exa_json_path=$..hostname,exa_regex=^({host}[\w\-.]+)$""",
"""exa_json_path=$..last_poll_ip,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
"""exa_json_path=$..infection.infection-type,exa_field_name=alert_type""",
"""exa_json_path=$..alert_id,exa_field_name=alert_id""",
"""exa_json_path=$..infection.confidence-level,exa_field_name=alert_severity""",
"""exa_json_path=$..applied-action,exa_field_name=action""",
"""exa_json_path=$..infected-object.file-object.file-path,exa_regex=^({file_path}(({file_dir}[^"]*?[\\\/]+)?({file_name}[^\\\/"]+?(\.({file_ext}\w+))?)))$""",
"""exa_json_path=$..user.username,exa_regex=^((?i)SYSTEM|({user}[\w\.\-]{1,40}\$?))$""",
"""exa_json_path=$..user.domain,exa_regex=^((?i)NT AUTHORITY|({domain}[^"]+))$""",
"""exa_json_path=$..infected-object.file-object.md5sum,exa_field_name=hash_md5""",
"""exa_json_path=$..infected-object.file-object.sha1sum,exa_field_name=hash_sha1""",
"""exa_json_path=$..infected-object.file-object.sha256sum,exa_field_name=hash_sha256"""
]
ParserVersion = "v1.0.0"


}
```
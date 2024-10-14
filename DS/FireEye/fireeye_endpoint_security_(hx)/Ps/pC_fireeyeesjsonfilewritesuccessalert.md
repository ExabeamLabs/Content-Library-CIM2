#### Parser Content
```Java
{
Name = "fireeye-es-json-file-write-success-alert"
Vendor = "FireEye"
Product = "FireEye Endpoint Security (HX)"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
ExtractionType = json
Conditions = [
""""hostname":"""
""""event_at":"""
""""event_type":"""
""""fileWriteEvent""""
""""fileWriteEvent/fileName":"""
""""alert_id":"""
]
Fields = [
"""exa_json_path=$.event_at,exa_field_name=time""",
"""exa_json_path=$.alert_id,exa_field_name=alert_id""",
"""exa_json_path=$..last_poll_ip,exa_regex=^({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?$""",
"""exa_json_path=$.event_id,exa_field_name=event_code""",
"""exa_json_path=$..hostname,exa_regex=^({host}[\w\-.]+)$""",
"""exa_json_path=$.event_type,exa_field_name=event_name""",
"""exa_json_path=$.event_values.fileWriteEvent/eventReason,exa_field_name=operation""",
"""exa_json_path=$.event_values.fileWriteEvent/fileName,exa_regex=({file_name}[^"]+?(\.({file_ext}[^"]+))?)$""",
"""exa_json_path=$.event_values.fileWriteEvent/username,exa_regex=^(({domain}[^"\\\/]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
"""exa_json_path=$.event_values.fileWriteEvent/fullPath,exa_field_name=file_path""",
"""exa_json_path=$.event_values.fileWriteEvent/process,exa_field_name=process_name""",
"""exa_json_path=$.event_values.fileWriteEvent/processPath,exa_field_name=process_dir"""
]
ParserVersion = "v1.0.0"


}
```
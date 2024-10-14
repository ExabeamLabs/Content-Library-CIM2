#### Parser Content
```Java
{
Name = fireeye-endpointsecurity-json-alert-trigger-success-processevent
    Vendor = FireEye
    Product = FireEye Endpoint Security (HX)
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    ExtractionType = json
    Conditions = [ """"event_at":""", """"event_type":""", """"processEvent"""", """"processEvent/pid":""", """"processEvent/process":""", """"alert_id":""" ]
    Fields = [
       """exa_json_path=$.event_at,exa_field_name=time""",
       """exa_json_path=$.alert_id,exa_field_name=alert_id""",
       """exa_json_path=$..last_poll_ip,exa_regex=^({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?$""",
       """exa_json_path=$..hostname,exa_regex=^({host}[\w\-.]+)$""",
       """exa_json_path=$.event_type,exa_field_name=alert_name""",
       """exa_json_path=$.event_values.processEvent/eventType,exa_field_name=event_name""",
       """exa_json_path=$.event_values.processEvent/processCmdLine,exa_field_name=process_command_line""",
       """exa_json_path=$.event_values.processEvent/md5,exa_field_name=hash_md5""",
       """exa_json_path=$.event_values.processEvent/process,exa_field_name=process_name""",
       """exa_json_path=$.event_values.processEvent/username,exa_regex=^(({domain}[^"\\\/]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)$"""
    ]
    DupFields = ["alert_name->alert_type"]
	ParserVersion = "v1.0.0"


}
```
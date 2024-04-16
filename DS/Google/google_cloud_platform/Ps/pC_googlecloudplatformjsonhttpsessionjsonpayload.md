#### Parser Content
```Java
{
Name = "google-cloudplatform-json-http-session-jsonpayload"
Vendor = "Google"
Product = "Google Cloud Platform"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""jsonPayload":"""
""""gce_instance""""
"""googleapis.com"""
"""resource_name"""
]
Fields = [
"""exa_json_path=$.timestamp,exa_field_name=time""",
"""exa_json_path=$.jsonPayload.bytes,exa_field_name=bytes"""
"""exa_json_path=$.jsonPayload.client,exa_regex=(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
"""exa_json_path=$.jsonPayload.method,exa_field_name=method""",
"""exa_json_path=$.jsonPayload.cache,exa_field_name=proxy_action""",
"""exa_json_path=$.jsonPayload.status,exa_field_name=http_response_code""",
"""exa_json_path=$.jsonPayload.url,exa_field_name=url""",
"""exa_json_path=$.jsonPayload.user,exa_field_name=user"""
"""exa_json_path=$.logName,exa_regex=.+squid_({action}[^"]+)"""
"""exa_json_path=$.resource.labels.project_id,exa_field_name=project_id"""
"""exa_json_path=$.jsonPayload.hierarchy_target,exa_regex=(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
"""exa_json_path=$.resource.labels.zone,exa_field_name=zone"""
"""exa_json_path=$.resource.labels.instance_id,exa_field_name=host"""
]
ParserVersion = "v1.0.0"


}
```
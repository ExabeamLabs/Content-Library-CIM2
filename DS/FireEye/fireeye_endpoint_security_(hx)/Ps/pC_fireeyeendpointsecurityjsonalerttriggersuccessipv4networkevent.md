#### Parser Content
```Java
{
Name = fireeye-endpointsecurity-json-alert-trigger-success-ipv4networkevent
    Vendor = FireEye
    Product = FireEye Endpoint Security (HX)
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    ExtractionType = json
    Conditions = [ """"hostname":""", """"event_at":""", """"event_type":""", """"ipv4NetworkEvent"""", """"ipv4NetworkEvent/remoteIP":""", """"alert_id":""", """"ipv4NetworkEvent/username":""" ]
    Fields = [
      """exa_json_path=$.event_at,exa_field_name=time""",
      """exa_json_path=$.alert_id,exa_field_name=alert_id""",
      """exa_json_path=$.event_type,exa_field_name=alert_name""",
      """exa_json_path=$..hostname,exa_regex=^({host}[\w\-.]+)$""",
      """exa_json_path=$.event_values.ipv4NetworkEvent/remoteIP,exa_regex=^({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?$""",
      """exa_json_path=$.event_values.ipv4NetworkEvent/remotePort,exa_field_name=dest_port""",
      """exa_json_path=$.event_values.ipv4NetworkEvent/processPath,exa_field_name=process_path""",
      """exa_json_path=$.event_values.ipv4NetworkEvent/process,exa_field_name=process_name""",
      """exa_json_path=$.event_values.ipv4NetworkEvent/protocol,exa_field_name=protocol""",
      """exa_json_path=$.event_values.ipv4NetworkEvent/localIP,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
      """exa_json_path=$.event_values.ipv4NetworkEvent/localPort,exa_field_name=src_port""",
      """exa_json_path=$.event_values.ipv4NetworkEvent/username,exa_regex=^(({domain}[^"\\\/]+)[\\\/]+)?({user}[\w\.\-]{1,40}\$?)$"""
    ]
    DupFields = ["alert_name->alert_type"]
	ParserVersion = "v1.0.0"
  

}
```
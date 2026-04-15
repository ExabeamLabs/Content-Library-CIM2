#### Parser Content
```Java
{
Name = "corelight-corelightids-json-app-activity-success-dce_rpc"
  ExtractionType = json
  Vendor = "Corelight"
  Product = "Corelight IDS"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"_path":""", """"_system_name":""", """ts":"""" ]
  Fields = [
    """exa_json_path=$.ts_start,exa_field_name=time""",
  	"""exa_json_path=$.ts,exa_field_name=time""",
  	"""exa_json_path=$._system_name,exa_field_name=sensor_name""",
  	"""exa_json_path=$._system_name,exa_field_name=host""",
  	"""exa_json_path=$._path,exa_field_name=event_subtype""",
  	"""exa_json_path=$.uid,exa_field_name=connection_id""",
  	"""exa_json_path=$.['id.orig_h'],exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
  	"""exa_json_path=$.['id.orig_p'],exa_field_name=src_port""",
  	"""exa_json_path=$.['id.resp_h'],exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
  	"""exa_json_path=$.['id.resp_p'],exa_field_name=dest_port""",
  	"""exa_json_path=$.operation,exa_field_name=operation""",
  	"""exa_json_path=$.endpoint,exa_field_name=interface_name"""
    """"ts_start":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,6}Z)""",
    """"ts":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,6}Z)""",
    """"_system_name":"({sensor_name}[\w\.\-]+)""",
     """"_system_name":"({host}[\w\.\-]+)""",
    """"_path":"({event_subtype}[^"]+)"""
    """"uid":"({connection_id}[^"]+)"""
    """"id\.orig_h":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """"id\.orig_p":({src_port}\d+)"""
    """"id\.resp_h":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """"id\.resp_p":({dest_port}\d+)"""
    """"operation":"({operation}[^"]+)""",
    """"endpoint":"({interface_name}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```
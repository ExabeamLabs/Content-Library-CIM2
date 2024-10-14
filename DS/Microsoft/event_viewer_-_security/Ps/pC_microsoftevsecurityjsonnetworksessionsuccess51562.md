#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-network-session-success-5156-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
ExtractionType = json
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss"]
Conditions = [
"""EventID":5156"""
"""The Windows Filtering Platform has permitted a connection"""
]
Fields = [
"""Hostname":\s*"({host}[^"]+)"""
"""ComputerName":\s*"({host}[^"]+)"""
""""TimeGenerated\\?":\\?"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""
""""EventTime"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
"""({event_code}5156)"""
"""({event_name}The Windows Filtering Platform has permitted a connection)"""
"""Layer Name:\s*(\\t|\\r|\\n)*({layer_name}[^\s\\]+)\s*(\\t|\\r|\\n)*Layer"""
"""Protocol":\s*"({ms_protocol_num}\d+)"""
"""ProcessID":\s*"({process_id}[^"]+)"""
"""Application":\s*"({process_path}({process_dir}[^"]+)[\\\/]({process_name}[^"]+))""""
"""Direction":\s*"({direction}[^"]+)""""
"""Direction:\s*[\\rtn]*({direction}(Inbound|Outbound))"""
"""DestAddress":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""DestPort":\s*"({dest_port}\d+)"""
"""SourceAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""SourcePort":\s*"({src_port}\d+)"""
"""exa_json_path=$.Hostname,exa_field_name=host"""
"""exa_json_path=$.Computer,exa_field_name=host"""
"""exa_json_path=$.times.[0],exa_field_name=time"""
"""exa_regex="TimeGenerated\\?":\\?"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""
"""exa_regex="EventTime"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""exa_json_path=$.EventID,exa_field_name=event_code"""
"""exa_json_path=$.Message,exa_field_name=event_name"""
"""exa_json_path=$..LayerName,exa_field_name=layer_name"""
"""exa_json_path=$..Protocol,exa_field_name=ms_protocol_num"""
"""exa_json_path=$..ProcessID,exa_field_name=process_id"""
"""exa_json_path=$..Application,exa_regex=({process_path}({process_dir}[^"]+)[\\\/]({process_name}[^"]+))"""
"""exa_json_path=$..Direction,exa_field_name=direction"""
"""exa_json_path=$..DestAddress,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
"""exa_json_path=$..DestPort,exa_field_name=dest_port"""
"""exa_json_path=$..SourceAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
"""exa_json_path=$..SourcePort,exa_field_name=src_port"""
]
ParserVersion = "v1.0.0"


}
```
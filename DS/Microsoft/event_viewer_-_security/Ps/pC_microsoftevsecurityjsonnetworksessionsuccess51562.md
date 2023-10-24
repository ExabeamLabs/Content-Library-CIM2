#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-network-session-success-5156-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""EventID":5156"""
"""The Windows Filtering Platform has permitted a connection"""
]
Fields = [
"""Hostname":\s*"({host}[^"]+)"""
"""ComputerName":\s*"({host}[^"]+)"""
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
]
ParserVersion = "v1.0.0"


}
```
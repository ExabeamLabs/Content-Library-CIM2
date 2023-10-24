#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-network-session-success-5156-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""event_id"""
""":5156"""
"""The Windows Filtering Platform has permitted a connection"""
]
Fields = [
""""name":[^,]+,"hostname":"({host}[^"]+)""""
""""hostname":"({host}[^"]+)""""
""""timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""""
"""({event_code}5156)"""
"""({event_name}The Windows Filtering Platform has permitted a connection)"""
"""LayerName\\*":\\*"({layer_name}[^"\\]+)\\*""""
"""Protocol\\*":\s*\\*"({ms_protocol_num}\d+)"""
"""ProcessID\\*":\s*\\*"({process_id}\d+)"""
"""Application\\*":\s*\\*"((System|({process_path}({process_dir}[^"]+)[\\\/]({process_name}[^"]+))))\\*""""
"""Direction:\s*(\\r|\\n|\\t)*({direction}(Inbound|Outbound))"""
"""DestAddress\\*":\s*\\*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\\*"""
"""DestPort\\*":\s*\\*"({dest_port}\d+)"""
"""SourceAddress\\*":\s*\\*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\\*"""
"""SourcePort\\*":\s*\\*"({src_port}\d+)"""
]
ParserVersion = "v1.0.0"


}
```
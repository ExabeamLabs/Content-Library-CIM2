#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-network-session-success-5156-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
"""EventID":5156"""
"""The Windows Filtering Platform has permitted a connection"""
]
Fields = [
"""Hostname":\s*"({host}[^"]+)"""
"""EventTime":\s*"({time}[^"]+)"""
"""({event_code}5156)"""
"""({event_name}The Windows Filtering Platform has permitted a connection)"""
"""Layer Name:\s*[\\trn]*({layer_name}[^\s]+)"""
"""Protocol":\s*"({ms_protocol_num}\d+)"""
"""ProcessID":\s*"({process_id}[^"]+)"""
"""Application":\s*"({process_path}({process_dir}[^"]+)[\\\/]({process_name}[^"]+))""""
"""Direction":\s*"({direction}[^"]+)""""
"""Direction:\s*[\\rtn]*({direction}(Inbound|Outbound))"""
"""DestAddress":\s*"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""DestPort":\s*"({dest_port}\d+)"""
"""SourceAddress":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""SourcePort":\s*"({src_port}\d+)"""
]
ParserVersion = "v1.0.0"


}
```
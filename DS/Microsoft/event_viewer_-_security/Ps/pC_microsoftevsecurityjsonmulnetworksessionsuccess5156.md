#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-mul-network-session-success-5156
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "yyyy-MM-dd HH:mm:ss", "epoch", "epoch_sec"]
  Conditions = [
"""5156""",
"""The Windows Filtering Platform has permitted a connection"""
  ]
  Fields = [
    """EventTime\":\"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\""""
    """Microsoft-Windows-Security-Auditing.*?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+(::ffff:)?(am|AM|pm|PM|({host}[\w.\-]+))"""
    """start=({time}\d{13})""",
    """TimeGenerated\\?=({time}\d{10})"""
    """\WComputer\*=(::ffff:)?({host}[\w\-.]+)"""
    """\WComputerName:\s*(::ffff:)?({host}[\w\-.]+)"""
    """({time}\w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+"""
    """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s(::ffff:)?(am|pm|\d{4}|({host}[\w\-.]+))\s"""
    """({event_code}5156)"""
    """({event_name}The Windows Filtering Platform has permitted a connection)"""
    """Process ID:((\\)*(\\r|\\t|\\n))*\s*({process_id}\d+)"""
    """Application Name:(\\r|\\n|\\t)*\s*([\\nrt]+System[\\nrt]+|({process_path}({process_dir}[^\t\n]+?)[\\\/]+({process_name}[^\\\/\t\n]+?)))(\\r|\\n|\\t)*\s*Network Information:"""
    """Direction:\s*({direction}Inbound).*Source Address:\s*(::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)\s*Source Port:\s*({dest_port}\d+)\s*Destination Address:\s*(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)\s*Destination Port:\s*({src_port}\d+)"""
    """Direction:\s*({direction}Outbound).*Source Address:\s*(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)\s*Source Port:\s*({src_port}\d+)\s*Destination Address:\s*(::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)\s*Destination Port:\s*({dest_port}\d+)"""
    """Protocol:\s*(\\r|\\n|\\t)*({ms_protocol_num}\d+)"""
    """Layer Name:(\\r|\\n|\\t)*\s*({layer_name}[^\s]+)"""
    """"hostname":"({host}[\w\-\.]+)""""
    """"ProcessID\\*":\s*\\*"({process_id}[^\\"]+)"""
    """"DestAddress\\*":\s*\\*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """"DestPort\\*":\\*"({dest_port}\d+)"""
    """"SourceAddress\\*":\\*\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """"SourcePort\\*":\\*"({src_port}\d+)"""
    """"Protocol\\*":\\*\s*"({ms_protocol_num}\d+)"""
    """"LayerName\\*":\\*"({layer_name}[^\\"]+)"""
  ]
  DupFields = [ "ms_protocol_num->protocol" ]


}
```
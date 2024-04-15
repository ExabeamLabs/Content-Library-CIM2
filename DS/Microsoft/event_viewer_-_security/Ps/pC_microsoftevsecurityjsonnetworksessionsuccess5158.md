#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-network-session-success-5158"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [
""""EventID":5158,"""
"""The Windows Filtering Platform has permitted a bind to a local port"""
  ]
  Fields = [
"""({event_code}5158)"""
"""({event_name}The Windows Filtering Platform has permitted a bind to a local port)"""
"""\"EventTime\"+:\s*\"+({time}[^\",]+)"""
"""\"Hostname\"+:\"+({host}[^\",]+)"""
"""\"ProcessId\"+:\"+({process_id}[^\"]+)"""
"""\"Application\"+:\"+({process_path}({process_dir}[^,\"]*?[\\\/]+)?({process_name}[^\\\/\s\"]+?))\""""
"""\"SourceAddress\"+:\"+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\"SourcePort\"+:\"+({dest_port}\d+)"""
"""\"Protocol\"+:\"+({ms_protocol_num}[^\"]+)"""
"""Layer Name:(?:\s|\\t|\\n|\\r)*({layer_name}[^:]+?)(?:\s|\\t|\\n|\\r)*Layer Run-Time ID:"""
"""(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|({dest_host}[\w\-.]+)))"""
  ]
  DupFields = [
"host->dest_host"
  ]


}
```
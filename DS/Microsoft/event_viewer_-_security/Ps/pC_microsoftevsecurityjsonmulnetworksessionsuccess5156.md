#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-mul-network-session-success-5156
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [
"""5156""",
"""The Windows Filtering Platform has permitted a connection"""
  ]
  Fields = [
    """EventTime\":\"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\""""
    """Microsoft-Windows-Security-Auditing.*?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+(::ffff:)?(am|AM|pm|PM|({host}[\w.\-]+))"""
    """(?i)\w+ \d+ \d\d:\d\d:\d\d (::ffff:)?(am |pm |({host}[\w\-.]+))\s+[A-Za-z]"""
    """\WComputer\*=(::ffff:)?({host}[\w\-.]+)"""
    """\WComputerName:\s*(::ffff:)?({host}[\w\-.]+)"""
    """({time}\w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+"""
    """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s(::ffff:)?(am|pm|({host}[\w\-.]+))"""
    """({event_code}5156)"""
    """({event_name}The Windows Filtering Platform has permitted a connection)"""
    """Process ID:\s*({process_id}\d+)"""
    """Application Name:\s*({process_path}({process_dir}[^\t\n]{1,2000}?)[\\\/]({process_name}[^\\\/\t\n]{1,2000}?))\s*Network Information:""",
    """Direction:\s*({direction}Inbound).*Source Address:\s*(::ffff:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)\s*Source Port:\s*({dest_port}\d+)\s*Destination Address:\s*(::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)\s*Destination Port:\s*({src_port}\d+)"""
    """Direction:\s*({direction}Outbound).*Source Address:\s*(::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)\s*Source Port:\s*({src_port}\d+)\s*Destination Address:\s*(::ffff:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)\s*Destination Port:\s*({dest_port}\d+)"""
    """Protocol:\s*({ms_protocol_num}\d+)"""
    """Layer Name:\s*({layer_name}[^\s]+)"""
  ]


}
```
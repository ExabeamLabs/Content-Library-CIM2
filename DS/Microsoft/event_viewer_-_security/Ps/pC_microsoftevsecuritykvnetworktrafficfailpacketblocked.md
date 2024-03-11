#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-network-traffic-fail-packetblocked
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """The Windows Filtering Platform has blocked a packet.""", """Application Name:""", """Layer Name:""" ]
  Fields = [
    """({event_name}The Windows Filtering Platform has blocked a packet)""",
    """Process ID:\s+({process_id}[^\s]+)\s+Application""",
    """Direction:\s+({direction}[^\s]+)\s+Source Address:""",
    """Source Address:\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Source Port:\s+({src_port}\d+)""",
    """Destination Address:\s+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """Destination Port:\s+({dest_port}\d+)"""
  ]


}
```
#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-network-session-success-5156
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product =  Event Viewer - Security
  TimeFormat = "epoch_sec"
  Conditions = [ """EventIDCode=5156""" ]
  Fields = [
    """Computer=\s*({host}[^\s]*)""",
    """EventID=({event_code}\d{1,100})""",
    """TimeGenerated=({time}\d{1,100})""",
    """Message=({event_name}.*?)\s*Application Information:""",
    """Process ID:\s*({process_id}\d{1,100})""",
    """Application Name:\s*({process_path}({process_dir}.+)[\\\/]({process_name}.+?))\s*Network Information:""",
    """Computer=\s*({dest_host}[^\s]*).*Direction:\s*({direction}Inbound).*Source Address:\s*({dest_ip}[^\s]*)\s*Source Port:\s*({dest_port}\d*)\s*Destination Address:\s*({src_ip}[^\s]*)\s*Destination Port:\s*({src_port}\d*)""",
    """Computer=\s*({src_host}[^\s]*).*Direction:\s*({direction}Outbound).*Source Address:\s*({src_ip}[^\s]*)\s*Source Port:\s*({src_port}\d*)\s*Destination Address:\s*({dest_ip}[^\s]*)\s*Destination Port:\s*({dest_port}\d*)""",
    """Protocol:\s*({ms_protocol_num}\d*)""",
    """Layer Name:\s*({layer_name}[^\s]*)"""
  ]


}
```
#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-network-session-success-5158
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security 
  TimeFormat = "epoch_sec"
  Conditions = [
"""EventIDCode=5158"""
  ]
  Fields = [
    """Computer=\s*({host}[^\s]*)"""
    """EventID=({event_code}\d+)"""
    """TimeGenerated=({time}\d{10})"""
    """Message=({event_name}.*?)\s*Application Information:"""
    """Process ID:\s*({process_id}\d+)"""
    """Application Name:\s*({process_path}({process_dir}.+)[\\/]({process_name}.+?))\s*Network Information:"""
    """Source Address:\s*({dest_ip}[^\s]*)\s*Source Port:\s*({dest_port}\d*)"""
    """Protocol:\s*({ms_protocol_num}\d*)"""
    """Layer Name:\s*({layer_name}.*?)\s*Layer Run-Time ID"""
  ]
  DupFields = [ "host->dest_host" ]


}
```
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
    """Computer=\s*({src_host}({host}[\w\-.]*))"""
    """EventID=({event_code}\d+)"""
    """TimeGenerated=({time}\d{10})"""
    """Message=({event_name}.*?)\s*Application Information:"""
    """Process ID:\s*({process_id}\d+)"""
    """Application Name:\s*({process_path}({process_dir}.+)[\\/]({process_name}.+?))\s*Network Information:"""
    """Source Address:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*Source Port:\s*({=src_port}\d*)"""
    """Protocol:\s*({protocol}\d+)"""
    """Layer Name:\s*({layer_name}.*?)\s*Layer Run-Time ID"""
  ]


}
```
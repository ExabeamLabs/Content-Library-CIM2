#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-network-session-fail-5157-1
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
Conditions = [
  """Exabeam Windows 5157"""
  """summary_windows_5157_data"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+[+-]\d+)"""
  """({event_code}5157)"""
  """summary_windows_5157_data="+\d+:\d+:\d+\s*\d+-\d+-\d+:::({event_code}[^:::]+)?:::({host}[^:::]+)?:::({process_id}[^:::]+)?:::({process_path}({process_dir}(?:.+?)?[\\\/])?({process_name}[^\\\/:::]+))?:::({src_ip}[^:::]+)?:::({src_port}\d+)?:::({dest_ip}[^:::]+)?:::({dest_port}\d+)?:::({protocol}[^:::]+)?:::({event_name}[^:::]+)?:::([^:::]+)?:::({direction}[^:::]+)?:::([^:::]+)?:::({layer_name}[^:::]+)?""""
]
DupFields = [
  "host->local_asset"
]
ParserVersion = "v1.0.0"


}
```
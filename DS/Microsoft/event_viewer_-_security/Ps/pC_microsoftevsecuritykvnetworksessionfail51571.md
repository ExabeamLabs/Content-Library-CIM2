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
  """summary_windows_5157_data="+\d+:\d+:\d+\s*\d+-\d+-\d+:::({event_code}[^:::]+)?:::({host}[^:::]+)?:::({process_id}[^:::]+)?:::({process_path}({process_dir}(?:.+?)?[\\\/])?({process_name}[^\\\/:::]+))?:::(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)?:::({=src_port}\d+)?:::(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)?:::({=dest_port}\d+)?:::({protocol}[^:::]+)?:::({event_name}[^:::]+)?:::([^:::]+)?:::({direction}[^:::]+)?:::([^:::]+)?:::({layer_name}[^:::]+)?""""
]
ParserVersion = "v1.0.0"


}
```
#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-network-session-success-5158-1
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """5158"""
  """<Data Name ='"""
  """The Windows Filtering Platform has permitted a bind to a local port"""
]
Fields = [
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """({event_code}5158)"""
  """"Activity":"({event_name}[^"]+)"""
  """"Computer":"({host}[^"]+)"""
  """<Data Name ='ProcessId'>({process_id}.+?)</Data>"""
  """<Data Name ='Application'>({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^"\\\/]+))</Data>"""
  """<Data Name ='SourceAddress'>(0\.0\.0\.0|({dest_ip}[a-fA-F:\d.]+))</Data>"""
  """<Data Name ='SourcePort'>({dest_port}\d+)"""
  """<Data Name ='Protocol'>({ms_protocol_num}.+?)</Data>"""
  """<Data Name ='LayerName'>({layer_name}.+?)</Data>"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```
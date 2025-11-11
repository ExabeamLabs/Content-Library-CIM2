#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-network-session-success-5158-1
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """5158"""
  """<Data Name"""
  """The Windows Filtering Platform has permitted a bind to a local port"""
]
Fields = [
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """({event_code}5158)"""
  """"Activity":"({event_name}[^"]+)"""
  """"Computer":"({src_host}({host}[\w\-.]+))"""
  """<Data Name\\*=('|")ProcessId('|")>({process_id}.+?)</Data>"""
  """<Data Name\\*=('|")Application('|")>({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^"\\\/]+))</Data>"""
  """<Data Name\\*=('|")SourceAddress('|")>(0\.0\.0\.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)</Data>"""
  """<Data Name\\*=('|")SourcePort('|")>({src_port}\d+)"""
  """<Data Name\\*=('|")Protocol('|")>({ms_protocol_num}.+?)</Data>"""
  """<Data Name\\*=('|")LayerName('|")>({layer_name}.+?)</Data>"""
  """<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```
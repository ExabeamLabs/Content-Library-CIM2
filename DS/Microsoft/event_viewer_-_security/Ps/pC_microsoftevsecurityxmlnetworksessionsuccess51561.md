#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-network-session-success-5156-1
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """"EventID":"5156""""
  """<Data Name"""
]
Fields = [
  """({event_name}The Windows Filtering Platform has allowed a connection)"""
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """({event_code}5156)"""
  """"Computer":"({host}[^"]+)"""
  """<Data Name\\*=('|")ProcessId('|")>({process_id}[^<>]+)<\/Data>"""
  """<Data Name\\*=('|")Application('|")>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/]+?))<\/Data>"""
  """<Data Name\\*=('|")SourceAddress('|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</Data>"""
  """<Data Name\\*=('|")SourcePort('|")>({src_port}\d+)</Data>"""
  """<Data Name\\*=('|")DestAddress('|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?</Data>"""
  """<Data Name\\*=('|")DestPort('|")>({dest_port}\d+)</Data>"""
  """<Data Name\\*=('|")Protocol('|")>({protocol}[^<>]+)</Data>"""
  """<Data Name\\*=('|")Direction('|")>({direction}[^<>]+)</Data>"""
  """<Data Name\\*=('|")LayerName('|")>({layer_name}[^<>]+)</Data>"""
  """<RenderingInfo.+?<Task>({operation_type}[^<>]+)</Task>.*?</RenderingInfo>"""
  """<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```
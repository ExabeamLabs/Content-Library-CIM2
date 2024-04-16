#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-network-session-fail-5157-1
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss"]
Conditions = [
  """"EventID":"5157""""
  """<Data Name"""
]
Fields = [
  """({event_name}The Windows Filtering Platform has blocked a connection)"""
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
  """({event_code}5157)"""
  """"Computer":"({host}[^"]+)"""
  """<Data Name\\*='ProcessID'>({process_id}[^<>]+)<\/Data>"""
  """<Data Name\\*='Application'>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/]+?))<\/Data>"""
  """<Data Name\\*='SourceAddress'>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</Data>"""
  """<Data Name\\*='SourcePort'>(0|({src_port}\d+))</Data>"""
  """<Data Name\\*='DestAddress'>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?</Data>"""
  """<Data Name\\*='DestPort'>(0|({dest_port}\d+))</Data>"""
  """<Data Name\\*='Protocol'>({protocol}[^<>]+)</Data>"""
  """<RenderingInfo.+?<Task>({operation_type}[^<>]+)</Task>.*?</RenderingInfo>"""
  """<Data Name\\*='Direction'>({direction}[^<>]+)</Data>"""
  """<Data Name\\*='LayerName'>({layer_name}[^<>]+)</Data>"""
  """<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```
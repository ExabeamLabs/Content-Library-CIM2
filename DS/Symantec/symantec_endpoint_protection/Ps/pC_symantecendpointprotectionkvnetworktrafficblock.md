#### Parser Content
```Java
{
Name = symantec-endpointprotection-kv-network-traffic-block
Vendor = "Symantec"
Product = "Symantec Endpoint Protection"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """Local:"""
  """Remote:"""
  """Rule:"""
  """Action:"""
  """Begin:"""
  """End:"""
  """Occurrences:"""
  """Application:"""
]
Fields = [
  """\WBegin:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d((\+|\-)\d\d:\d\d)?)"""
  """({host}[\w\-\.]+)\s*SymantecServer:"""
  """,Local:\s*({src_ip}[a-fA-F:\.\d]+),Local:\s*({src_port}\d+),Local:\s*(0.0.0.0|({=src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w\-\.]+)),"""
  """,Remote:\s*(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?),Remote:\s*(|({dest_host}[\w\-\.]+)),Remote:\s*({=dest_port}\d+),"""
  """({protocol}[^,]+),({direction}[^,]+),Begin:"""
  """\WApplication:\s*({process_path}({process_dir}[^",]+?)?([\\\/]+({process_name}[^\\\/,"]+)))\s*,"""
  """\WRule:\s*({event_name}[^,]+)"""
  """\WAction:\s*({action}[^,]+?)"*\s*$"""
  """\WUser:\s*(none|({user}[^,]+)),Domain:\s*(|({domain}[^,]+?))\s*,"""
]
ParserVersion = "v1.0.0"


}
```
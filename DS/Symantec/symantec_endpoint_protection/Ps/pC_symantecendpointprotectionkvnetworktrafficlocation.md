#### Parser Content
```Java
{
Name = symantec-endpointprotection-kv-network-traffic-location
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """SymantecServer""", """Remote Host Name: """, """Local Host IP: """, """Action: """ ]
  Fields = [
  """SymantecServer:\s({host}[\w\-.]+)"""
  """Local Host IP:\s*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),Local Port:\s({dest_port}\d+).*?,Inbound,"""
  """Local Host IP:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),Local Port:\s({src_port}\d+).*?,Outbound,"""
  """Remote Host IP:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),Remote Host Name:\s({src_host}[\w\-.]+),.*?,Inbound,"""
  """Remote Host IP:\s*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),Remote Host Name:\s({dest_host}[\w\-.]+),.*?,Outbound,"""
  """Action:\s({action}[^"$]+)"""
  """({direction}Inbound|Outbound)"""
  """Application:\s*({process_path}({process_dir}[^,]*?[\\\/]+)({process_name}[^,\\\/]+)),"""
  ]


}
```
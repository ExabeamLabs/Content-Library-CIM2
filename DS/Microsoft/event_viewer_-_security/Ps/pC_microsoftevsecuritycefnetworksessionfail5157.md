#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-network-session-fail-5157"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [
"""5157"""
"""The Windows Filtering Platform has blocked a connection"""
  ]
  Fields = [
"""\Wrt=({time}\d+)"""
"""({event_name}The Windows Filtering Platform has blocked a connection)"""
"""({event_code}5157)"""
"""ComputerName:\s*({host}[\w.\-]+)"""
"""\sProcess ID:\s*(|({process_id}\d+))\s*Application Name:\s*(|({process_path}({process_dir}.*?[\\\/]+)?({process_name}[^\\\/]+?)))\s*Network Information:"""
"""\sDirection:\s*({direction}\S+)"""
"""\sSource Address:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sSource Port:\s*({src_port}\d+)"""
"""\sDestination Address:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sDestination Port:\s*({src_port}\d+)"""
"""\sProtocol:\s*({protocol}\S+)"""
"""\sLayer Name:\s*(|({layer_name}.+?))\s*Layer Run-Time ID:"""
"""\sUser:\s*(N/A|({user}.+?))\s*ComputerName:"""
  ]
  DupFields = [
"host->local_asset"
  ]


}
```
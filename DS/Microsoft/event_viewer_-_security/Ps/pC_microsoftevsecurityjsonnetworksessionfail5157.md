#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-network-session-fail-5157"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [
""""EventID":5157"""
"""The Windows Filtering Platform has blocked a connection"""
  ]
  Fields = [
"""\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s[^\s]+\s"""
"""({event_name}The Windows Filtering Platform has blocked a connection)"""
"""({event_code}5157)"""
"""ComputerName:\s*({host}[\w.\-]+)"""
"""Process ID:\s*(\\t|\\r|\\n)*(|({process_id}\d+))\s*(\\t|\\r|\\n)*Application Name:\s*(\\t|\\r|\\n)*(|({process_path}({process_dir}.*?[\\\/]+)?({process_name}[^\\\/]+?)))\s*(\\t|\\r|\\n)*Network Information:"""
"""Direction:\s*(\\t|\\r|\\n)*({direction}[^:]+?)(\\t|\\r|\\n)*Source Address:"""
"""Source Address:\s*(\\t|\\r|\\n)*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(\\t|\\r|\\n)*"""
"""Source Port:\s*(\\t|\\r|\\n)*({src_port}\d+)(\\t|\\r|\\n)*"""
"""Destination Address:\s*(\\t|\\r|\\n)*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?(\\t|\\r|\\n)*"""
"""Destination Port:\s*(\\t|\\r|\\n)*({dest_port}\d+)(\\t|\\r|\\n)*"""
"""Protocol:\s*(\\t|\\r|\\n)*({protocol}[^:]+?)(\\t|\\r|\\n)*Filter Information:"""
"""Layer Name:\s*(\\t|\\r|\\n)*(|({layer_name}.+?))\s*(\\t|\\r|\\n)*Layer Run-Time ID:"""
"""User:\s*(\\t|\\r|\\n)*(N/A|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*(\\t|\\r|\\n)*ComputerName:"""
  ]


}
```
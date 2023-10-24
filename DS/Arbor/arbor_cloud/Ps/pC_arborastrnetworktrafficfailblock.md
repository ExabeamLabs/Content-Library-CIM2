#### Parser Content
```Java
{
Name = "arbor-a-str-network-traffic-fail-block"
Vendor = "Arbor"
Product = "Arbor Cloud"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
"""arbor-networks-aps:"""
"""Blocked Host"""
]
Fields = [
  """\d\d:\d\d:\d\d\s({host}[^\s]*)\s""",
  """Blocked\shost\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sby\s({failure_reason}.+)\susing""",
  """\susing\s({protocol}[^\/]*)\/\d+\s"""
  """destination\s({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s""",
  """\ssource\sport\s({src_port}\d+)"""
  """\w+\/({dest_port}\d+)\s\("""
  """\/\d+\s\(({operation}[^\)]*)""",
  """arbor-networks-aps:\s*({action}[^:]*):\s"""
]
ParserVersion = "v1.0.0"


}
```
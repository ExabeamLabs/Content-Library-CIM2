#### Parser Content
```Java
{
Name = "checkpoint-ngfw-str-network-traffic-success-accept-2"
  ParserVersion = "v1.0.0"
  Vendor = "Check Point"
  Product = "Check Point NGFW"
  TimeFormat = "epoch_sec"
  Conditions = [""" CheckPoint """, """action:Accept""", """product:VPN-1 & FireWall-1"""]
  Fields = [
"""\stime:({time}\d{10})\""""
"""\d\d:\d\d:\d\dZ\s*({host}[\w\-\.]+)\s*CheckPoint"""
"""cu_rule_category:({operation}[^\"]+)\""""
"""event_name:({event_name}[^\"]+)\""""
"""cu_rule_id:\{({rule_id}[^\"]+?)\}\""""
"""action:({result}Accept)"""
"""cu_detected_by:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\""""
"""dst:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\""""
"""proto:({protocol}[^\"]+)\""""
"""service:({dest_port}\d+)\""""
  ]


}
```
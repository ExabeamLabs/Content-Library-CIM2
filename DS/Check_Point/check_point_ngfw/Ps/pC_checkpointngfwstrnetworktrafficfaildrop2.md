#### Parser Content
```Java
{
Name = "checkpoint-ngfw-str-network-traffic-fail-drop-2"
  ParserVersion = "v1.0.0"
  Vendor = "Check Point"
  Product = "Check Point NGFW"
  TimeFormat = "epoch_sec"
  Conditions = [""" CheckPoint """, """ origin:""", """product=VPN-1 & FireWall-1""", """action:Drop";"""]
  Fields = [
"""\Wtime:({time}\d{10})"""
"""\W({host}[\w\-.]+) CheckPoint"""
"""src_machine_name:({src_host}[\w\-.]+)"""
"""\Wsrc:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wxlatesrc:(0\.0\.0\.0|({src_translated_ip}[A-Fa-f:\d.]+))"""
"""\Wdst:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wxlatedst:(0\.0\.0\.0|({dest_translated_ip}[A-Fa-f:\d.]+))"""
"""\Wservice_id:({app_protocol}[^\"\;]+)"""
"""\Waction:({result}Drop)"""
"""\Wrule_name:({rule}[^\"\;]+?)\s*\";"""
"""\Ws_port:({src_port}\d+)"""
"""\Wxlatesport:({src_translated_port}\d+)"""
"""\Wxlatedport:({dest_translated_port}\d+)"""
"""\Wifdir:({direction}[^\"]+)"""
"""\Wservice:({dest_port}\d+)"""
"""\Wproto:({protocol}[^\"\;]+)"""
"""\Wrule_uid:\{?({rule_id}[^\"\}\;]+)"""
"""\Wpolicy_name=({rule}[^\"]+?)\\]"""
  ]


}
```
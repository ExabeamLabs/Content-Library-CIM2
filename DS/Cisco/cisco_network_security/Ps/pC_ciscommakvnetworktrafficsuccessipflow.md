#### Parser Content
```Java
{
Name = "cisco-mma-kv-network-traffic-success-ip-flow"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco"
  Product = Cisco Network Security
  TimeFormat = "epoch_sec"
  Conditions = [
""" ip_flow_start"""
""" src="""
""" dst="""
  ]
  Fields = [
"""(<\d+>[^\s]+)?\s+({time}\d{10})\.\d+\s({event_name}[^\s]+?)\ssrc="""
"""(<\d+>[^\s]+)?\s+({time}\d{10})\.\d+\s"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sprotocol=({protocol}\w+)"""
"""\ssport=({src_port}\d+)"""
"""\sdport=({dest_port}\d+)"""
"""\smac=({src_mac}[a-fA-F\d.:]+)"""
"""\stranslated_src_ip=({src_translated_ip}[a-fA-F\d.:]+)\stranslated_port=({src_translated_port}\d+)"""
"""\stranslated_dst_ip=({dest_translated_ip}[a-fA-F\d.:]+)\stranslated_port=({dest_translated_port}\d+)"""
  ]


}
```
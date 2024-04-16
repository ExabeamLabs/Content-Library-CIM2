#### Parser Content
```Java
{
Name = "cisco-mma-kv-network-traffic-flows"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco" 
  Product = "Cisco Meraki MX appliance"
  TimeFormat = "epoch_sec"
  Conditions = [
""" flows """
""" src="""
""" dst="""
  ]
  Fields = [
"""start=({time}\d{10})"""
"""({time}\d{10})\.\d+\s+({host}[\w.\-]+)\s+flows\s"""
"""\d\d:\d\d:\d\d ({host}[\w.\-]+) ({time}\d+)\.\d+ \S+\s+flows\s"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sprotocol=({protocol}\w+)"""
"""\ssport=({src_port}\d+)"""
"""\sdport=({dest_port}\d+)"""
"""\sflows\s+({result}\w+)\s"""
"""\spattern:\s*({result}\w+)"""
"""\smac=({src_mac}[a-fA-F\d.:]+)"""
  ]


}
```
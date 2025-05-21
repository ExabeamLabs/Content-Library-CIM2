#### Parser Content
```Java
{
Name = "f5-bigip-kv-network-traffic-success"
ParserVersion = "v1.0.0"
Vendor = "F5"
Product = "F5 BIG-IP"
TimeFormat = ["MMM  d HH:mm:ss","MMM dd HH:mm:ss"]
Conditions = [
"""f5_irule"""
"""src_ip="""
"""vip_ip="""
"""snat_port="""
"""vip_name="""
"""node_ip="""
"""node_port="""
]
  Fields = [
    """({time}\w+\s+\d+\s+\d\d:\d\d:\d\d)\s+({host}[\w\-\.]+) tmm""",
    """src_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """src_port=({src_port}\d+)""",
    """vip_name=({interface_name}[^,]+)"""
    """snat_ip=({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """snat_port=({src_translated_port}\d+)"""
  ]


}
```
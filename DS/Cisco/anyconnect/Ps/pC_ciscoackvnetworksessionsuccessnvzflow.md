#### Parser Content
```Java
{
Name = cisco-ac-kv-network-session-success-nvzflow
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = AnyConnect
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """ pn=""", """ ppn=""", """fv=nvzFlow_v3""" ]
  Fields = [
    """\sfet='*(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d\d:\d\d:\d\d \d+)""",
    """\ssa="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\ssa="({host}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """\sda="({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\ssp=({src_port}\d+)""",
    """\sdp=({dest_port}\d+)""",
    """\sibc=({bytes_in}\d+)""",
    """\sobc=({bytes_out}\d+)""",
    """\spr=({packet_rate}\d+)""",
    """\spn='*(?=\w)({process_name}[^']+)'*\s""",
    """\sppn='*(?=\w)({parent_process_name}[^']+)'*\s""",
    """\spph="({parent_process_hash}([^"]+))"""",
    """\sdh="({dest_host}([^"]+))"""",
    """\sph="?({process_hash}([^\s]+))"?\s""",
    """\sppap='(?:[^']+[\s])?'*({user}[^\s']+)""",
    """\sppaa='(?:[^']+[\s])?'*({domain}[^\s']+)""",
    """\spaa='(?:[^']+[\s])?'(?:[^']+[\s])?({domain}[^\s']+)""",
    """\spap='(?:[^']+[\s])?'(?:[^']+[\s])?({user}[^\s']+)""",
    """\sudid=({udid}([^\s]+))\s""",
    """\smnl='(?=\w)({module_hash_names}[^']+?)\s{0,100}'\s""",
    """\svsn=({virtual_station_name}[^\s]+)\s""",
    """\sosn=({os}[^\s]+)""",
    """\sosv=({os_version}[^\s]+)\s""",
    """\sose=({os_environment}[^\s]+)\s""",
    """\ssm=({system_manufacturer}[^\s]+)\s""",
    """\sst=({system_type}[^\s]+)\s"""
  ]


}
```
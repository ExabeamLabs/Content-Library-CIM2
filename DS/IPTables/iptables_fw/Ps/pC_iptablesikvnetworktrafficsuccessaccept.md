#### Parser Content
```Java
{
Name = iptables-i-kv-network-traffic-success-accept
  ParserVersion = v1.0.0
  Vendor = IPTables
  Product = IPTables FW
  TimeFormat = ["MMM dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """ kernel: """, """ ACCEPT """ ]
  Fields = [
    """({time}\w+\s+\d+ \d+:\d+:\d+)"""
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({host}[\w.\-]+)\s+kernel:\s""",
    """\sIN=({src_interface}[^=]+?)\s+\w+=""",
    """\sOUT=({dest_interface}[^=]+?)\s+\w+=""",
    """\sMAC=({src_mac}[^=]+?)(\s+\w+=|\s*$)""",
    """\sSRC=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sDST=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sPROTO=({protocol}[^=]+?)\s+\w+=""",
    """\sSPT=({src_port}\d+)""",
    """\sDPT=({dest_port}\d+)""",
  ]


}
```
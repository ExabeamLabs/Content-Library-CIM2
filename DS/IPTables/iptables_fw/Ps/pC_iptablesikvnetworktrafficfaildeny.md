#### Parser Content
```Java
{
Name = iptables-i-kv-network-traffic-fail-deny
  ParserVersion = v1.0.0
  Vendor = IPTables
  Product = IPTables FW
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """ kernel: """, """ DENY """ ]
  Fields = [
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({host}[\w.\-]+)\s+kernel:\s""",
    """\sIN=({src_interface}[^=]+?)(\s+\w+=|\s*$)""",
    """\sOUT=({dest_interface}[^=]+?)(\s+\w+=|\s*$)""",
    """\sMAC=({src_mac}[^=]+?)(\s+\w+=|\s*$)""",
    """\sSRC=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sDST=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sPROTO=({protocol}[^=]+?)(\s+\w+=|\s*$)""",
    """\sSPT=({src_port}\d+)""",
    """\sDPT=({dest_port}\d+)""",
  ]


}
```
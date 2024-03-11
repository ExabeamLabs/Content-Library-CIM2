#### Parser Content
```Java
{
Name = iptables-fw-json-network-traffic-fwiptable
    ParserVersion = "v1.0.0"
    Vendor = IPTables
    Product = IPTables FW
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = [ """"logT":"FW-IPTables"""" ]
    Fields = [
      """"host":"({host}[^"]+)""",
      """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
      """\sIN=({src_interface}[^=]+?)\s+(\w+=|\\n")""",
      """\sOUT=({dest_interface}[^=]+?)\s+(\w+=|\\n")""",
      """\sMAC=({src_mac}[^=]+?)\s+(\w+=|\\n")""",
      """\sSRC=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))\s+(\w+=|\\n")""",
      """\sDST=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))\s+(\w+=|\\n")""",
      """\sPROTO=({protocol}[^=]+?)\s+(\w+=|\\n")""",
      """\sSPT=({src_port}\d+)\s+(\w+=|\\n")""",
      """\sDPT=({dest_port}\d+)\s+(\w+=|\\n")""",
    ]
  

}
```
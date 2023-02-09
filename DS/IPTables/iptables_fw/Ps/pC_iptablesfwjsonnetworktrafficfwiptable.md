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
      """\sSRC=({src_ip}[a-fA-F\d.:]+)\s+(\w+=|\\n")""",
      """\sDST=({dest_ip}[a-fA-F\d.:]+)\s+(\w+=|\\n")""",
      """\sPROTO=({protocol}[^=]+?)\s+(\w+=|\\n")""",
      """\sSPT=({src_port}\d+)\s+(\w+=|\\n")""",
      """\sDPT=({dest_port}\d+)\s+(\w+=|\\n")""",
    ]
  

}
```
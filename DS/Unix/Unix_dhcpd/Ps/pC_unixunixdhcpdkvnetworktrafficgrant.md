#### Parser Content
```Java
{
Name = unix-unixdhcpd-kv-network-traffic-grant
  Vendor = Unix
  Product = Unix dhcpd
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ dhcpd: """, """ GRANT """ ]
  Fields = [
    """\w+ \d+ \d\d:\d\d:\d\d ({host}[\w.\-]+) dhcpd:""",
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({event_name}GRANT)""",
    """\sIP=({dest_ip}[a-fA-F\d.:]+)""",
    """\sMAC=({dest_mac}[a-fA-F\d.:]+)""",
    """\sHOSTNAME=(?:nil|({dest_host}.+?))\s+\w+=""",
    """\sDOMAIN=({domain}.+?)\s+\w+=""",
    """\sLEASETIME=({lease_time}.+?)\s+\w+="""
  ]
  DupFields = [ "dest_host->user" ]


}
```
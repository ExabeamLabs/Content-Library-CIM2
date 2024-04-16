#### Parser Content
```Java
{
Name = unix-unixdhcpd-kv-network-traffic-grant
  Vendor = Unix
  Product = Unix dhcpd
  ParserVersion = "v1.0.0"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","MMM dd HH:mm:ss"]
  Conditions = [ """ dhcpd: """, """ GRANT """ ]
  Fields = [
    """({time}\w+ \d+ \d\d:\d\d:\d\d)? ({host}[\w.\-]+) dhcpd:""",
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({event_name}GRANT)""",
    """\sIP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sMAC=({dest_mac}[a-fA-F\d.:]+)""",
    """\sHOSTNAME=(?:nil|({dest_host}.+?))\s+\w+=""",
    """\sDOMAIN=({domain}.+?)\s+\w+=""",
    """\sLEASETIME=({lease_time}.+?)\s+\w+="""
  ]
  DupFields = [ "dest_host->user" ]


}
```
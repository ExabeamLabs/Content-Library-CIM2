#### Parser Content
```Java
{
Name = fortinet-firewall-kv-dhcp-session-success-dhcpacklog
  Vendor = Fortinet
  Product = Fortinet Enterprise Firewall
  TimeFormat = "yyyy-MM-dd' time='HH:mm:ss"
  Conditions = [ """ logver=""", """ logdesc="""", """ dhcp_msg="""" ]
  Fields = [
    """\Wdate=({time}\d\d\d\d\-\d\d\-\d\d time\=\d\d:\d\d:\d\d)""",
    """\w+ \d+ \d\d:\d\d:\d\d ({host}[\w\-.]+)""",
    """\Wip=({dest_ip}[a-fA-F:\d.]+)""",
    """\Whostname="({dest_host}[\w\-.]+)""",
    """\Whostname="({user}[^"\s]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```
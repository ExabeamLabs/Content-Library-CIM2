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
    """\Wip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Whostname="({dest_host}[\w\-.]+)""",
    """\Whostname="({user}[^"\s]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```
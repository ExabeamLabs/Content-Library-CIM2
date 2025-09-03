#### Parser Content
```Java
{
Name = fortinet-fortigate-cef-network-traffic-success-trafficipconn
  Vendor = Fortinet
  Product = FortiGate
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """|Fortinet|FortiGate""", """|forward traffic ip-conn|""" ]
  Fields = [
    """\w{3}\s+\d{1,2}\s+\d\d:\d\d:\d\d\s+({host}[\w\-.]+)\sCEF""",
    """start=({time}\w{3}\s\d{2}\s\d{4}\s\d{2}:\d{2}:\d{2})""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """spt=({src_port}\d+)""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """dpt=({dest_port}\d+)""",
    """act=({action}[^=]+)\s[\w\.]+=""",
    """CEF:([^|]+\|){5}({event_name}[^|]+)\|""",
    """deviceSeverity=({additional_info}[^=]+?)\s+([\w.]+=|$)"""
   ]


}
```
#### Parser Content
```Java
{
Name = unix-unixnamed-str-app-activity-success-lameservers
  Vendor = Unix
  Product = Unix Named
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd HH:mm:ss"
  Conditions = [ """ named[""", """: FORMERR resolving '""" ]
  Fields = [
    """({time}\w+\s\d+\s\d+:\d+:\d+)"""
    """\s({host}\S+)\s+named\[""",
    """named\[\S+?:\s+({additional_info}[^~]+)"""
    """({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\#({src_port}\d+)""",
    """: ({event_name}FORMERR[^']*?)\s*'({dns_query}[^'\/]+)""",
  ]


}
```
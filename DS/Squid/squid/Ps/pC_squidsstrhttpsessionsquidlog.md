#### Parser Content
```Java
{
Name = squid-s-str-http-session-squidlog
  Vendor = "Squid"
  Product = "Squid"
  TimeFormat = "epoch_sec"
  Conditions = [ """ SQUID_LOG """ ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s+SQUID_LOG""",
    """SQUID_LOG\s+({time}\d{10})\.\d{3}""",
    """SQUID_LOG\s+\S+\s*({duration}\d+)""",
    """SQUID_LOG\s+(\S+\s*){2}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """SQUID_LOG\s+(\S+\s*){3}(?:\w+\/)({http_response_code}\d+)""",
    """SQUID_LOG\s+(\S+\s*){4}({bytes_out}\d+)""",
    """SQUID_LOG\s+(\S+\s*){5}({method}\S+)""",
    """SQUID_LOG\s+(\S+\s*){6}(?:({protocol}\w+\:\/+))?({web_domain}[^\s:\/]+)(?:\:({dest_port}\d+))?""",
    """SQUID_LOG\s+(\S+\s*){7}(-|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """SQUID_LOG\s+(\S+\s*){8}(HIER_)?({hierarchy_code}[^\/]+)\/({dest_local_host}[^\/\s]+)\s""",
    """SQUID_LOG\s+(\S+\s*){9}(-|({mime}[^$\s]+))\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```
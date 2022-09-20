#### Parser Content
```Java
{
Name = nortelcontivity-vpn-str-vpn-logout-exceedtimeout
Vendor = Nortel Contivity
Product = Nortel Contivity VPN
ParserVersion = "v1.0.0"
TimeFormat = "MM/dd/yyyy HH:mm:ss"
Conditions = ["""tIsakmp""", """exceeded idle timeout""" ]
Fields = [ """\w+\s+\d+ \d+:\d+:\d+ ({host}[\w.\-]+)""",
"""({time}\d+/\d+/\d+ \d+:\d+:\d+)""",
"""({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}) has exceeded idle timeout - logging out""" ]


}
```
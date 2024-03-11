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
"""({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+)) has exceeded idle timeout - logging out""" ]


}
```
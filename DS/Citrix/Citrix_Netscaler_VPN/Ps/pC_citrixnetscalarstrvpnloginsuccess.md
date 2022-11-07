#### Parser Content
```Java
{
Name = citrix-netscalar-str-vpn-login-success
    ParserVersion = v1.0.0
    Vendor = Citrix
    Product = Citrix Netscaler VPN
    TimeFormat = "MM/dd/yyyy:HH:mm:ss"  
    Conditions = [ """SSLVPN ICASTART""", """username:domainname""" ]
    Fields = [
      """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[\w\-.]+)""",
      """({time}\d\d/\d\d/\d\d\d\d:\d\d:\d\d:\d\d)""",
      """username:domainname\s({user}[^:@]+)(:|@)({domain}[^\s]+[^\s:])?""",
      """Source\s({src_ip}[\w.:]+[^:]):\d+""",
      """Destination\s({dest_ip}[^:]+)""",
      """applicationName\s({app}.+?) - startTime"""
    ]
  

}
```
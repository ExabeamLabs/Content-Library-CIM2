#### Parser Content
```Java
{
Name = barracuda-firewall-kv-vpn-login-success-accountinglogin
  ParserVersion = v1.0.0
  Vendor = Barracuda
  Product = Barracuda Firewall
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """ CP-FW Session """, """ Accounting LOGIN """ ]
  Fields = [
    """\sCP-FW Session\s+\S*?({user}[^\-:]+):""",
    """\suser=(|({user}.+?))(\s+\w+=|\s*$)""",
    """\sIP=({src_ip}[a-fA-F\d.:]+)""",
    """\sstart="({time}\d\d\d\d/\d\d/\d\d \d\d:\d\d:\d\d)""",
  ]


}
```
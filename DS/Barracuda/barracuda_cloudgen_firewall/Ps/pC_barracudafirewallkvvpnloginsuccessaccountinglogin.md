#### Parser Content
```Java
{
Name = barracuda-firewall-kv-vpn-login-success-accountinglogin
  ParserVersion = v1.0.0
  Vendor = Barracuda
  Product = Barracuda Cloudgen Firewall
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """ CP-FW Session """, """ Accounting LOGIN """ ]
  Fields = [
    """\sCP-FW Session\s+\S*?({user}[^\-:]+):""",
    """\suser=(|({user}.+?))(\s+\w+=|\s*$)""",
    """\sIP=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sstart="({time}\d\d\d\d/\d\d/\d\d \d\d:\d\d:\d\d)""",
  ]


}
```
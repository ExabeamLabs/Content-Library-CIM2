#### Parser Content
```Java
{
Name = barracuda-firewall-kv-vpn-login-success-peerlogin
  ParserVersion = v1.0.0
  Vendor = Barracuda
  Product = Barracuda Cloudgen Firewall
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """ CP-FW Session """, """ Login peer=""" ]
  Fields = [
    """\sCP-FW Session\s+\S*?({user}[^\-:]+):""",
    """\speer=({src_translated_ip}[a-fA-F\d.:]+)""",
    """\sserver=(|({dest_host}.+?))(\s+\w+=|\s*$)""",
  ]


}
```
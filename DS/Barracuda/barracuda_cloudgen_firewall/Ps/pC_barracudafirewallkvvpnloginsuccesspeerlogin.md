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
    """\speer=({src_translated_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """\sserver=(|({dest_host}.+?))(\s+\w+=|\s*$)""",
  ]


}
```
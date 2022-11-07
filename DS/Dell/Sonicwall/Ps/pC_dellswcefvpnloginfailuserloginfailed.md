#### Parser Content
```Java
{
Name = dell-sw-cef-vpn-login-fail-userloginfailed
  ParserVersion = v1.0.0
  Vendor = Dell
  Product = Sonicwall
  TimeFormat = "epoch"
  Conditions = [ """|Sonicwall|VPN|""", """|User login failed""" ]
  Fields = [
    """\srt=({time}\d+)""",
    """\sdvc=({host}\S+)""",
    """\sdvchost=({host}\S+)""",
    """\ssrc=({src_ip}\S+)""",
    """\sdst=({dest_ip}\S+)""",
    """\sdhost=({dest_host}\S+)""",
    """\sduser=(|({user}.+?))\s+(\w+=|$)""",
    """\|User login failed - ({failure_reason}.+?)\|""",
  ]


}
```
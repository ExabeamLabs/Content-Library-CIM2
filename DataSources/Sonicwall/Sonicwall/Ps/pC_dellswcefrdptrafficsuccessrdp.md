#### Parser Content
```Java
{
Name = dell-sw-cef-rdp-traffic-success-rdp
  Vendor = Sonicwall
  Product = Sonicwall
  TimeFormat = "epoch"
  Conditions = [ """|Sonicwall|VPN|""", """cs2Label=Protocol""", """cs2=RDP"""]
  Fields = [
    """\srt=({time}\d+)""",
    """\sdvc=({host}\S+)""",
    """\sdvchost=({host}\S+)""",
    """\ssrc=({src_ip}\S+)""",
    """\sdst=({dest_ip}\S+)""",
    """\sdhost=({dest_host}\S+)""",
    """\sduser=(|({user}.+?))\s+(\w+=|$)""",
    """\scs2=(|({login_type_text}.+?))\s+(\w+=|$)""",
  ]
  ParserVersion = v1.0.0


}
```
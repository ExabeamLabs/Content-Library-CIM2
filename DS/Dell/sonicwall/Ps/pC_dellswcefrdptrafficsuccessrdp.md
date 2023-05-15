#### Parser Content
```Java
{
Name = dell-sw-cef-rdp-traffic-success-rdp
  Vendor = Dell
  Product = Sonicwall
  TimeFormat = "epoch"
  Conditions = [ """|Sonicwall|VPN|""", """cs2Label=Protocol""", """cs2=RDP"""]
  Fields = [
    """\srt=({time}\d{13})""",
    """\sdvc=({host}\S+)""",
    """\sdvchost=({host}\S+)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sdhost=({dest_host}\S+)""",
    """\sduser=(|({user}.+?))\s+(\w+=|$)""",
    """\scs2=(|({login_type_text}.+?))\s+(\w+=|$)""",
  ]
  ParserVersion = v1.0.0


}
```
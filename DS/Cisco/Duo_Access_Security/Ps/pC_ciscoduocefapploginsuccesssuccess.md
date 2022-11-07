#### Parser Content
```Java
{
Name = cisco-duo-cef-app-login-success-success
  Vendor = Cisco
  Product = Duo Access Security
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Duo Security|Two-Factor|""", """|SUCCESS|""" ]
  Fields = [
    """\|Duo Security\|({login_type_text}[^\|]+)\|[^\|]*\|({result}[^\|]+)\|""",
    """\scat=({additional_info}.+?)\s+(\w+=|$)""",
    """\srt=({time}\d+)""",
    """\ssrc=({src_ip}[a-fA-F\d.:]+)""",
    """\ssuser=({user}.+?)\s+(\w+=|$)""",
    """\ssproc=({app}.+?)\s+(\w+=|$)""",
    """\sdvc=({host}.+?)\s+(\w+=|$)""",
    """\sdvchost=({host}.+?)\s+(\w+=|$)""",
  ]


}
```
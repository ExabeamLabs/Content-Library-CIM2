#### Parser Content
```Java
{
Name = cisco-duo-cef-app-login-success-success
  Vendor = Cisco
  Product = Duo Access
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Duo Security|Two-Factor|""", """|SUCCESS|""" ]
  Fields = [
    """\|Duo Security\|({login_type_text}[^\|]+)\|[^\|]*\|({result}[^\|]+)\|""",
    """\scat=({additional_info}.+?)\s+(\w+=|$)""",
    """\srt=({time}\d{13})""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)""",
    """\ssproc=({app}.+?)\s+(\w+=|$)""",
    """\sdvc=({host}.+?)\s+(\w+=|$)""",
    """\sdvchost=({host}.+?)\s+(\w+=|$)""",
  ]


}
```
#### Parser Content
```Java
{
Name = "imperva-securesphere-cef-app-login-success-userloggedin"
  ParserVersion = "v1.0.0"
  Vendor = "Imperva"
  Product = "Imperva SecureSphere"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """|Imperva Inc.|SecureSphere""", """cat=SystemEvent""", """|User logged in|""" ]
  Fields = [
    """\srt=({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)""",
    """0\|([^\|]*\|){4}.+?logged in from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """0\|([^\|]*\|){4}User ({user}[\w\.\-\!\#\^\~]{1,40}\$?) logged in from""",
    """\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*(\w+=|$)"""
  ]


}
```
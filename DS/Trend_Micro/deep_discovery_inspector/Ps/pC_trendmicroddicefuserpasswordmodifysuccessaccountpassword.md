#### Parser Content
```Java
{
Name = trendmicro-ddi-cef-user-password-modify-success-accountpassword
  Vendor = Trend Micro
  Product = Deep Discovery Inspector
  TimeFormat = "MMM dd yyyy HH:mm:ss zZ"
  Conditions = [ """CEF:""", """|Trend Micro|Deep Discovery Inspector|""", """dvc=""", """Changed account password""" ]
  Fields = [
    """\Wdvc=({host}.+?)(\s+\w+=|\s*$)""",
    """\Wdvchost=({host}.+?)(\s+\w+=|\s*$)""",
    """\Wrt=({time}\w+\s+\d\d \d\d\d\d \d\d:\d\d:\d\d \S+)""",
    """\Wduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """\Woutcome=({result}.+?)\s+(\w+=|$)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ]
  ParserVersion = "v1.0.0"


}
```
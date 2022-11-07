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
    """\Wduser=({user}[^\s]+)""",
    """\Woutcome=({result}.+?)\s+(\w+=|$)""",
    """\Wsrc=({src_ip}[a-fA-F\d.:]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```
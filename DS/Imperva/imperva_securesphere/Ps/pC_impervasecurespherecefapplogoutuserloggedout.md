#### Parser Content
```Java
{
Name = imperva-securesphere-cef-app-logout-userloggedout
  Vendor = Imperva
  Product = Imperva SecureSphere
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """|Imperva Inc""", """|SecureSphere|""", """|User logged out|""" ]
  Fields = [
    """SecureSphere\|[^|]+?\|({operation}[^\|]+)\|({event_name}[^\|]+)\|({severity}[^\|]+)\|""",
    """\ssuser=({user}[\w\.\-]{1,40}\$?)(\s+\w+=|\s*$)""",
    """\srt=({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)""",
  ]
  ParserVersion = "v1.0.0"


}
```
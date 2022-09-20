#### Parser Content
```Java
{
Name = trendmicro-iws-cef-app-activity-success-6494263011
    ParserVersion = v1.0.0
    Conditions = [ """|McAfee|ESM""", """283-3423998809""" ]
  
n-forwarded-cef-trendmicro-system-event = {
  Vendor = Trend Micro
  Product = InterScan Web Security
  TimeFormat = "epoch"
  Fields = [
    """\Wrt=({time}\d+)""",
    """\Wcat=({category}.+?)(\s+\w+=|\s*$)""",
    """\Wdst=({dest_ip}[a-fA-F\d.:]+)""",
    """\Wsrc=({src_ip}[a-fA-F\d.:]+)""",
    """\Wshost=({src_host}.+?)(\s+\w+=|\s*$)""",
    """CEF:([^\|]*\|){5}({event_name}[^\|]+)""",
    """\WeventId=({event_code}\d+)""",
  
}
```
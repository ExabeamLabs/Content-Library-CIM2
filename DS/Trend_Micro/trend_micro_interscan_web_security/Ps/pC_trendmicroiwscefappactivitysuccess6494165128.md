#### Parser Content
```Java
{
Name = trendmicro-iws-cef-app-activity-success-6494165128
    ParserVersion = v1.0.0
    Conditions = [ """|McAfee|ESM""", """283-3731912406""" ]
  
n-forwarded-cef-trendmicro-system-event = {
  Vendor = Trend Micro
  Product = Trend Micro InterScan Web Security
  TimeFormat = "epoch"
  Fields = [
    """\Wrt=({time}\d{13})""",
    """\Wcat=({category}.+?)(\s+\w+=|\s*$)""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wshost=({src_host}.+?)(\s+\w+=|\s*$)""",
    """CEF:([^\|]*\|){5}({event_name}[^\|]+)""",
    """\WeventId=({event_code}\d+)""",
  
}
```
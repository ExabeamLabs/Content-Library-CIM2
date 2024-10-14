#### Parser Content
```Java
{
Name = trendmicro-ddi-kv-app-activity-success-systemevent
  Conditions = [ """CEF:""", """|Trend Micro|""", """|SYSTEM_EVENT|""" ]
  ParserVersion = "v1.0.0"

cef-trendmicro-system-event = {
    Vendor = Trend Micro
    Product = Deep Discovery Inspector
    TimeFormat = "MMM dd yyyy HH:mm:ss ZZZZ"
    Fields = [
      """({host}[\w.\-]+)\s+CEF:([^\|]*\|){5}({event_name}[^\|]+)""",
      """\Wrt=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d \w+(\+|\-)\d\d:\d\d)""",
      """\Wmsg=(|({additional_info}.+?))(\s+\w+=|\s*$)""",
      """\Wdvchost=(|({host}.+?))(\s+\w+=|\s*$)""",
# host_mac is removed
      """\Wdvc=({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    
}
```
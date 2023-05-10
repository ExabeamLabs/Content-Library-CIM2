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
      """\Wmsg=(|({event_description}.+?))(\s+\w+=|\s*$)""",
      """\Wdvchost=(|({host}.+?))(\s+\w+=|\s*$)""",
# host_mac is removed
      """\Wdvc=({host_ip}[a-fA-F\d:.]+)""",
    
}
```
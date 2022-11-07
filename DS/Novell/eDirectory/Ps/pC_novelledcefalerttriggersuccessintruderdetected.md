#### Parser Content
```Java
{
Name = novell-ed-cef-alert-trigger-success-intruderdetected
  Conditions = [ """CEF:""", """|eDirectory|eDirectory|""", """|INTRUDER_DETECTED|""" ]
  Fields = ${eDirectoryParsersTemplates.cef-edirectory-events.Fields} [
    """CEF:([^\|]*\|){5}({alert_name}[^\|]+)""",
    """CEF:([^\|]*\|){6}({alert_severity}[^\|]+)""",
    """sproc=({process_name}.*?)\s\w+=""", 
  ]
  DupFields = [ "alert_name->alert_type" ]
  ParserVersion = "v1.0.0"

cef-edirectory-events = {
  Vendor = Novell
  Product = eDirectory
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields = [
    """\Wrt=({time}\w+\s+\d+\s+\d+ \d\d:\d\d:\d\d)""",
    """\Wdvc=({host}[A-Fa-f:\d.]+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
    """\Wspt=({src_port}\d+)""",
    """\Wsuser=CN\=({src_host}[\w\-.]+)""",
    """\Wduser=CN\=({full_name}[^,]+),({user_ou}OU\=.+?)\s+(\w+=|$)""",
    """\Woutcome=({result}\w+)""",
    """\Wcs1=(({protocol}\w+):\s*)?({dest_ip}[A-Fa-f:\d.]+?):({dest_port}\d+)""",
  
}
```
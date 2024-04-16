#### Parser Content
```Java
{
Name = fireeye-endpointsecurity-cef-alert-trigger-containment
  ParserVersion = v1.0.0
  Vendor = FireEye
  Product = FireEye Endpoint Security (HX)
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF:""", """|fireeye|hx|""", """|FireEye """, """ Containment """ ]
  Fields = [
    """rt=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """dvchost=({host}[^.\s]+)""",
    """dst=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dhost=({src_host}[^\s]+)""",
    """suser=({email_address}[^@\s]+@[^\s,]+)""",
    """msg=({additional_info}[^=]+)\s+\w+=""",
    """({app}hx)""",
    """CEF:([^\|]*\|){4}({operation}[^\|]+)""",
    """request=({resource}[^\s=]+)\s*(\w+=|$)""",
    """act=({category}[^=]+)\s+\w+=""",
    """categoryOutcome=(\/)?({result}[^\s]+)"""
 ]
 DupFields = [ "resource->object", "operation->event_name" ]


}
```
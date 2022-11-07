#### Parser Content
```Java
{
Name = vmware-carbonblackappctrl-cef-app-activity-carbonblackevent
  ParserVersion = "v1.0.0"
  Vendor = VMware
  Product = Carbon Black App Control
  Conditions = [ """CEF:""", """|Carbon Black|App Control|""" ]

cef-carbonblack-events = {
  Vendor = VMware
  TimeFormat = "epoch"
  Fields = [
    """CEF:([^\|]*\|){5}({event_name}[^\|]+)\|({alert_severity}[^\|]+)\|""",
    """\Wmsg=(|({event_description}.+?))(\s+\w+=|\s*$)""",
    """\Wdhost=(|(({domain}[^\\\/=]+?)[\\\/]+)?({dest_host}.+?))(\s+\w+=|\s*$)""",
    """\Wdst=({dest_ip}[a-fA-F\d.:]+)""",
    """\Wdvchost=(|({host}.+?))(\s+\w+=|\s*$)""",
    """\Wrt=({time}\d+)""",
    """\Wcs3=(|({policy_name}.+?))(\s+\w+=|\s*$)""",
  
}
```
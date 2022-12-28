#### Parser Content
```Java
{
Name = vmware-edr-cef-app-notification-error
  ParserVersion = v1.0.0
  Product = Carbon Black EDR 
  Conditions = [ """CEF:""", """|Carbon Black|Protection|""", """|Agent error|""" ]

cef-carbonblack-events = {
  Vendor = VMware
  TimeFormat = "epoch"
  Fields = [
    """CEF:([^\|]*\|){5}({event_name}[^\|]+)\|({alert_severity}[^\|]+)\|""",
    """\Wmsg=(|({event_description}.+?))(\s+\w+=|\s*$)""",
    """\Wdhost=(|(({domain}[^\\\/=]+?)[\\\/]+)?({dest_host}.+?))(\s+\w+=|\s*$)""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wdvchost=(|({host}.+?))(\s+\w+=|\s*$)""",
    """\Wrt=({time}\d{13})""",
    """\Wcs3=(|({policy_name}.+?))(\s+\w+=|\s*$)""",
  
}
```
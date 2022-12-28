#### Parser Content
```Java
{
Name = mcafee-nsp-cef-alert-trigger-success-securitymanager
  Vendor = McAfee
  Product = McAfee Network Security Platform
  TimeFormat = "epoch"
  Conditions = [ """CEF:""" , """|McAfee|Network Security Manager|""", """ src=""" ]
  Fields = [
    """CEF:([^\|]*\|){5}({protocol}[^:\|]+):\s*({alert_name}[^\|]+)\|({alert_severity}[^\|]+)""",
    """\Wrt=({time}\d{13})""",
    """\Wdvc=({host}\S+)""",
    """\Wdvchost=({host}\S+)""",
    """\WeventId=({alert_id}\d+)""",
    """\Wcat=({alert_type}.+?)\s+(\w+=|$)""",
    """\Wact=(Unknown|({action}.+?))\s+(\w+=|$)""",
    """\Wapp=({app_protocol}.+?)\s+(\w+=|$)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wshost=({src_host}[\w\-.]+)""",
    """\Wdhost=({dest_host}[\w\-.]+)""",
    """\Wspt=({src_port}\d+)""",
    """\Wdpt=({dest_port}\d+)""",
  ]
  DupFields = [ "alert_name->policy_name" ]
  ParserVersion = "v1.0.0"


}
```
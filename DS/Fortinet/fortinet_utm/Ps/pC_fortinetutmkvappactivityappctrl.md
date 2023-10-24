#### Parser Content
```Java
{
Name = fortinet-utm-kv-app-activity-appctrl
  Vendor = Fortinet
  Product = Fortinet UTM
  TimeFormat = "yyyy-MM-dd';time='HH:mm:ss"
  Conditions = [ """;subtype=app-ctrl;""", """;devname=""",""";vd=""", """;date=""", """;applist=""" ]
  Fields = [
    """date=({time}\d\d\d\d-\d\d-\d\d;time=\d\d:\d\d:\d\d)""",
    """devname=({host}[\w\-\.]+)""",
    """subtype=({event_subtype}[^;]+)""",
    """srcip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dstip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """srcport=({src_port}\d{1,5})""",
    """dstport=({dest_port}\d{1,5})""",
    """;srcintf=({src_interface}[^;]+)""",
    """;dstintf=({dest_interface}[^;]+)""",
    """;proto=({protocol}\d{1,5})""",
    """direction=({direction}[^;]+)""",
    """policyid=({policy_id}\d+)""",
    """;app=({app}[^;]+)""",
    """action=({action}[^;]+)""",
    """hostname=({web_domain}[^;]+)""",
    """;appcat=({category}[^;]+)""",
    """;url=({uri_path}\/[^;]+)""",
    """subtype=({event_name}[^;]+)"""
  ]
  DupFields = [ "action->operation" ]
  ParserVersion = "v1.0.0"


}
```
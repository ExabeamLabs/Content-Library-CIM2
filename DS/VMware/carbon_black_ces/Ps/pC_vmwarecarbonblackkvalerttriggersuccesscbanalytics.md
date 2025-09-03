#### Parser Content
```Java
{
Name = vmware-carbonblack-kv-alert-trigger-success-cbanalytics
  Vendor = VMware
  Product = Carbon Black CES
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """CEF:""", """|CarbonBlack|""", """cat=CB_ANALYTICS""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}Z)""",
    """\|CarbonBlack\|((.*?)\|){2}({alert_type}.+?)\|""",
    """\|CarbonBlack\|((.*?)\|){3}({alert_name}.+?)\|""",
    """\|CarbonBlack\|((.*?)\|){3}({alert_severity}\d+)\|""",
    """\Wcat=({category}[^\|]+?)\s*(\||\w+=|$|"+\s*$)""",
    """\Wact=({action}[^\|]+?)\s*(\||\w+=|$|"+\s*$)""",
    """\Woutcome=({result}.+?)\s*(\w+=|$)""",
    """\WthreatAttackID=({threat_id}[^:]+?)\s*(\w+=|$|:)"""
  ]
  DupFields = [ "threat_id->alert_id" ]
  ParserVersion = "v1.0.0"


}
```
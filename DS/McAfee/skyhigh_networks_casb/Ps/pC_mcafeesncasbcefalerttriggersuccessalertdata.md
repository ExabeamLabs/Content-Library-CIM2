#### Parser Content
```Java
{
Name = mcafee-sncasb-cef-alert-trigger-success-alertdata
  Vendor = McAfee
  Product = Skyhigh Networks CASB
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
  Conditions = [  """Alert.Data""", """activityName =""", """actorIdType=""", """serviceNames=""", """|McAfee|MVISION Cloud|""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}[\w\.\-]+)""",
    """\|start=({time}\w{3} \d\d \d\d\d\d \d\d:\d\d:\d\d\.\d{1,3} \w{1,3})""",
    """response=\[({result}[^\]\s]+)""",
    """riskSeverity=({alert_severity}[^\s]+)""",
    """\ssuser=(({email_address}[^@\s=]+@[^\s=\.]+\.[^\s=]+)|({user}[\w\.\-]{1,40}\$?))\s+\w+=""",
    """({alert_type}Alert\.Data)""",
    """\|McAfee\|MVISION Cloud\|[^\|]+\|({alert_name}[^\|]+)\|""",
    """userAction=({action}[^=]+?)\s\w+=""",
    """incidentId=({alert_id}[^=]+?)\s\w+=""",
    """serviceNames=\[?(|({additional_info}[^=\]]+?))\]?\s+\w+=""",   
    """\sdhost=({dest_host}[\w\.\-]+)""",
    """activityName =\[({alert_activity}[^\]]+?)\]"""
  ]
  ParserVersion = v1.0.0


}
```
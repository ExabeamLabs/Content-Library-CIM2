#### Parser Content
```Java
{
Name = "mcafee-sncasb-kv-alert-trigger-success-actoridtype"
  Vendor = McAfee
  Product = Skyhigh Networks CASB
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
  ParserVersion = "v1.0.0"
    Conditions = [  """cat=Alert.Policy.Dlp""", """activityName =""", """actorIdType=""", """devTime=""", """ Cloud|""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}[^\s]+)""",
    """devTime=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d\.\d+ \w+)""",
    """src=(0\.0\.0\.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """policyName =({alert_name}[^=]+?)\s+\w+=""",
    """policyId=({alert_id}[^\s]+)""",
    """contentItemName =({file_name}[^=]+)\s+\w+=""",
    """response=\[({result}[^\]\s]+)""",
    """FileSize=({bytes}\d+)""",
    """riskSeverity=({alert_severity}[^\s]+)""",
    """({additional_info}totalMatchCount=[^\s]+)""",
    """contentItemId=({target}[^=]+?)\s+\w+=""",
    """instanceName =({src_host}[^=]+?)\s+\w+=""",
    """usrName =(({email_address}[^@]+@[^@\s]+)|({user}[\w\.\-]{1,40}\$?))\s+sev""",
    """activityName =\[({alert_type}[^\]]+?)\]"""
  ]


}
```
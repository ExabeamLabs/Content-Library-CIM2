#### Parser Content
```Java
{
Name = mcafee-sncasb-leef-alert-trigger-success-anomaly
  Vendor = McAfee
  Product = Skyhigh Networks CASB
  ParserVersion = "v1.0.0" 
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
  Conditions = [ """LEEF:""", """|Anomaly|""", """usrName =""", """devTime=""", """cat="""]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}[^\s]+)""",
    """devTime=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d\.\d+ \w+)""",
    """src=(0\.0\.0\.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """response=\[({result}[^\]\s]+)""",
    """usrName =(({email_address}[^@]+@[^@\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+=""",
    """activityName =\[({operation}[^\]\s]+)""",
    """userInfoFirstName =({first_name}[^\s]+)""",
    """userInfoLastName =({last_name}[^\s]+)""",
    """objectName =({object}[^=]+?)\s+\w+=""",
    """auditEventTypeEventTypeName =({operation}[^=]+?)\s+\w+=""",
    """serviceNames=\[({app}[^\]]+)""",
    """eventInfo=({additional_info}[^=]+?)\s+\w+="""
    """cat=({category}[^\s=\|]+)"""
    """incidentRiskSeverity=({alert_severity}[^\s=\|"]+)"""
    """incidentId=({alert_id}[^=]+?)\s\w+="""
  ]


}
```
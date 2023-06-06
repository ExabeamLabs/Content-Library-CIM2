#### Parser Content
```Java
{
Name = mcafee-sncasb-cef-alert-trigger-success-superhumanalertaccess-1
    ParserVersion = v1.0.0
    Vendor = McAfee
    Product = Skyhigh Networks CASB
    TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
    Conditions = [ """CEF:""", """McAfee""", """|Anomalies""", """|Superhuman|Alert.Access|""" ]
    Fields = [
      """\d\d:\d\d:\d\d\s({host}[\w.\-]+)\s+CEF""",
      """start=({time}\w{3} \d+ \d+ \d\d:\d\d:\d\d\.\d{3} \w{3})""",
      """suser=(N\/A|system:anonymous|({email_address}[^@=]+?@[^@=]+?)|({user}[^\s=]+?))\s""",
      """activityName =\[?({operation}[^=]+?)\].*?=""",
      """informationAnomalyCategory=({alert_type}[^=]+?)\s\w+=""",
      """CEF([^\|]*\|){6}({alert_severity}[^|]+)""", 
      """incidentId=({alert_id}[^=]+?)\s\w+="""
    ]
 

}
```
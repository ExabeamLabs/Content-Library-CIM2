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
      """suser=(N\/A|system:anonymous|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s""",
      """activityName =\[?({operation}[^=]+?)\].*?=""",
      """informationAnomalyCategory=({alert_type}[^=]+?)\s\w+=""",
      """CEF([^\|]*\|){6}({alert_severity}[^|]+)""", 
      """incidentId=({alert_id}[^=]+?)\s\w+="""
      """riskSeverity=({alert_severity}[^\s=\|]+)"""
    ]
 

}
```
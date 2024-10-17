#### Parser Content
```Java
{
Name = mcafee-sncasb-cef-alert-trigger-success-superhumanalertaccess
    ParserVersion = v1.0.0
    Vendor = McAfee
    Product = Skyhigh Networks CASB
    TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
    Conditions = [ """Skyhigh Security""", """Access Anomalies""", """Superhuman""", """Alert.Access""" ]
    Fields = [
      """\d\d:\d\d:\d\d\s({host}[\w.\-]+)\s+""",
      """end=({time}\w{3} \d+ \d+ \d\d:\d\d:\d\d\.\d{3} \w{3})""",
      """suser=(N\/A|system:anonymous|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s""",
      """msg=({alert_name}[^=]+?)\s\w+=""",
      """informationThreatCategory=({alert_type}[^=]+?)\s\w+=""",
      """CEF([^\|]*\|){6}({alert_severity}[^|]+)""", 
      """flexString2=({alert_id}[^\s]+)[^~]+?flexString2Label=incidentId""",
      """cs6=\[[^\]=]+?\.({operation}[^\]]+)[^~]+?cs6Label=Activity"""
      """devTime=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d\.\d+ \w+)""",
      """src=(0\.0\.0\.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
      """response=\[({result}[^\]\s]+)""",
      """usrName =(({email_address}[^@]+@[^@\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+=""",
      """activityName =\[({operation}[^\]\s]+)""",
      """serviceNames=\[({app}[^\]]+)""",
      """cat=({category}[^\s=\|]+)"""
      """riskSeverity=({alert_severity}[^\s=\|]+)"""
    ]
 

}
```
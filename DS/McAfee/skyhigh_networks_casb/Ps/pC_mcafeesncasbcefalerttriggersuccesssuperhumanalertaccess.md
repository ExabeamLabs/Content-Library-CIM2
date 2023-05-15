#### Parser Content
```Java
{
Name = mcafee-sncasb-cef-alert-trigger-success-superhumanalertaccess
	  ParserVersion = v1.0.0
    Vendor = McAfee
    Product = Skyhigh Networks CASB
    TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
    Conditions = [ """CEF:""", """Skyhigh Security""", """|Anomalies""", """|Superhuman|Alert.Access|""" ]
    Fields = [
      """\d\d:\d\d:\d\d\s({host}[\w.\-]+)\s+CEF""",
      """end=({time}\w{3} \d+ \d+ \d\d:\d\d:\d\d\.\d{3} \w{3})""",
      """suser=(N\/A|system:anonymous|({email_address}[^@=]+?@[^@=]+?)|({user}[^\s=]+?))\s""",
      """msg=({alert_name}[^=]+?)\s\w+=""",
      """informationThreatCategory=({alert_type}[^=]+?)\s\w+=""",
      """CEF([^\|]*\|){6}({alert_severity}[^|]+)""", 
      """flexString2=({alert_id}[^\s]+)[^~]+?flexString2Label=incidentId""",
      """cs6=\[[^\]=]+?\.({operation}[^\]]+)[^~]+?cs6Label=Activity"""
    ]
 

}
```
#### Parser Content
```Java
{
Name = mcafee-sncasb-cef-alert-trigger-success-dlpalertpolicy
	  ParserVersion = v1.0.0
    Vendor = Skyhigh Security
    Product = Skyhigh CASB
    TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
    Conditions = [ """CEF:""", """Skyhigh Security""", """|Anomalies""", """|Dlp|Alert.Policy|""" ]
    Fields = [
      """\d\d:\d\d:\d\d\s({host}[\w.\-]+)\s+CEF""",
      """CEF:([^\|]*\|){5}({alert_type}[^\|\s]+)\|""",
      """end=({time}\w{3} \d+ \d+ \d\d:\d\d:\d\d\.\d{3} \w{3})""",
      """suser=(N\/A|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s""",
      """CEF([^\|]*\|){6}({alert_severity}[^|]+)""", 
      """cs1=\[({result}[^\]]+)[^~]+?cs1Label=Responses""",
      """flexString2=({alert_id}[^\s]+)[^~]+?flexString2Label=incidentId""",
      """cs6=\[({operation}[^\s\]]+)[^~]+?cs6Label=Activity""",
      """instanceName =({src_host}[^\s]+?)\s""",
      """fname=({file_name}[^=]+?(\.({file_ext}[^\s=.]+))?)\s\w+="""
    ]
 

}
```
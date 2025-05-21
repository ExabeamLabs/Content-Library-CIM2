#### Parser Content
```Java
{
Name = mcafee-sncasb-cef-file-download-success-anomalousaccesslocation
    ParserVersion = v1.0.0
    Vendor = Skyhigh Security
    Product = Skyhigh CASB
    TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
    Conditions = [ """CEF:""", """Skyhigh Security""", """|Anomalies""", """|AnomalousAccessLocation|Alert.Access|""", """File downloaded""" ]
    Fields = [
      """\d\d:\d\d:\d\d\s({host}[\w.\-]+)\s+CEF""",
      """end=({time}\w{3} \d+ \d+ \d\d:\d\d:\d\d\.\d{3} \w{3})""",
      """suser=(N\/A|system:anonymous|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s""",
      """({event_name}File downloaded)""",
      """cs4=\[({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\]"""
	]


}
```
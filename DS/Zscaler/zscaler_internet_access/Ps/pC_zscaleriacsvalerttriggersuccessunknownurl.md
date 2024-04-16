#### Parser Content
```Java
{
Name = zscaler-ia-csv-alert-trigger-success-unknownurl
  ParserVersion = "v1.0.0"
  Vendor = Zscaler
  Product = Zscaler Internet Access
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ ""","Unknown URL",""" ]
  Fields = [
    """({time}\w{3} \d\d \d\d:\d\d:\d\d \d\d\d\d)""",
    """"({company}[^"]+)",("[^"]*",){12}"Unknown URL"""",
    """"({app}[^"]+)",("[^"]*",){11}"Unknown URL"""",
    """"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))",("[^"]*",){10}"Unknown URL"""",
    """"({department}[^"]+)",("[^"]*",){9}"Unknown URL"""",
    """"({file_name}[^"]+)",("[^"]*",){7}"Unknown URL"""",
    """"({file_path}[^"]+)",("[^"]*",){6}"Unknown URL"""",
    """({alert_name}Unknown URL)""",
    """"Unknown URL",("[^"]*",)"({bytes_in}\d+)""",
    """"Unknown URL",("[^"]*",){2}"({bytes_out}\d+)"""
  ]


}
```
#### Parser Content
```Java
{
Name = "lookout-l-cef-alert-trigger-success-threat"
  ParserVersion = "v1.0.0"
  Vendor = "Lookout"
  Product = "Lookout"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF:""", """|Lookout|""", """|THREAT|""" ]
  Fields = [
	  """rt=({time}\w\w\w\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
	  """CEF:([^|]+\|){4}({additional_info}[^|]+)""",
	  """CEF:([^|]+\|){6}({alert_severity}[^|]+)""",
	  """sourceServiceName =({os}[^=]+)\s\w+=""",
	  """suser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
	  """cat=({alert_name}[^=]+?)\s\w+=""",
    """act=({action}[^=]+)\s\w+=""",
    """cat=({alert_type}[^=]+?)\s\w+=""",
  ]


}
```
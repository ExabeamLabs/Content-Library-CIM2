#### Parser Content
```Java
{
Name = "lookout-l-cef-endpoint-notification-success-device"
  ParserVersion = "v1.0.0"
  Vendor = "Lookout"
  Product = "Lookout"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF:""", """|Lookout|""", """|DEVICE|""" ]
  Fields = [
	  """rt=({time}\w\w\w\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
	  """CEF:([^|]+\|){4}({additional_info}[^|]+)""",
	  """sourceServiceName =({os}[^=]+)\s\w+=""",
	  """suser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  ]


}
```
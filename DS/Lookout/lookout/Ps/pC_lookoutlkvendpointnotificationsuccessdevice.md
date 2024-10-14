#### Parser Content
```Java
{
Name = "lookout-l-kv-endpoint-notification-success-device"
  ParserVersion = "v1.0.0"
  Vendor = "Lookout"
  Product = "Lookout"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """details.type=""", """type=DEVICE,""", """details.activationStatus=""" ]
  Fields = [
	  """eventTime=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
	  """target.emailAddress=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
	  """target.platform=({os}[^,]+)"""
  ]


}
```
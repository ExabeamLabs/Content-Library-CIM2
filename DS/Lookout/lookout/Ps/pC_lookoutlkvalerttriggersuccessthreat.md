#### Parser Content
```Java
{
Name = "lookout-l-kv-alert-trigger-success-threat"
  ParserVersion = "v1.0.0"
  Vendor = "Lookout"
  Product = "Lookout"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """type=THREAT,""", """details.severity=""", """details.classifications=""" ]
  Fields = [
	  """eventTime=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
	  """\sid=({alert_id}[^,]+)""",
	  """details.severity=({alert_severity}[^,]+)""",
	  """details.classifications=({alert_name}[^,]+)""",
    """details.type=({alert_type}[^,]+)""",
	  """target.emailAddress=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
	  """target.platform=({os}[^,]+)"""
	  """details.action=({action}[^,]+)""",
    """, details.type=({additional_info}[^,]+)"""
  ]


}
```
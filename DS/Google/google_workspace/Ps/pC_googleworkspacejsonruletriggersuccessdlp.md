#### Parser Content
```Java
{
Name = google-workspace-json-rule-trigger-success-dlp
  ParserVersion = v1.0.0
  Vendor = Google
  Product = Google Workspace
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"applicationName":"rules"""", """"DLP-SourceCode"""", """"DLP"""",  """"rule_name"""" ]
  Fields = [
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"profileId":"({user_id}\d+)""",
    """"actor":\{.*?"email"\s*:\s*"({email_address}({user}[^@"]+)@[^"]+)"""",
    """"name".*?"data_source".*?"value":"({app}[^"]+)"""",
	""""resource_id".*?"value":"({resource_id}[^"]+)"""",
	""""rule_name".*?"value":"({rule}[^"]+)"""",
	""""rule_type".*?"value":"({alert_type}[^"]+)"""",
	""""severity".*?"value":"({rule_severity}[^"]+)"""",
	""""resource_type".*?"value":"({resource_type}[^"]+)""""
  ]


}
```
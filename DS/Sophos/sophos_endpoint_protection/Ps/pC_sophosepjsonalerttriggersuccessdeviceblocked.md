#### Parser Content
```Java
{
Name = sophos-ep-json-alert-trigger-success-deviceblocked
  ParserVersion = v1.0.0
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"Event::Endpoint::Device::Blocked""", """"name": "Peripheral """ ]
  Fields = [
    """"rt":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """\s"name":\s*"({alert_name}[^"':]+)""",
    """"name":\s*"({additional_info}[^"]+)""",
    """"type":\s*"({alert_type}[^"]+)""",
    """"dhost":\s*"({src_host}[^"]+)""",
    """"severity":\s*"({alert_severity}[^"]+)""",
    """"suser":\s*"(?:n\/a|({full_name}[^"\\]+))"""",
    """"suser":\s*"(?:n\/a|({user}[\w\.\-]{1,40}\$?))"""",
    """"suser":\s*"(({domain}[^\\",]+)\\+)?({user}[\w\.\-]{1,40}\$?)"""",
    """"id":\s*"({alert_id}[^"]+)""",
  ]


}
```
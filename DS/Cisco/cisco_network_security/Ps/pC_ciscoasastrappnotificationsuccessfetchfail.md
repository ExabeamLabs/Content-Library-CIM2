#### Parser Content
```Java
{
Name = cisco-asa-str-app-notification-success-fetchfail
    ParserVersion = v1.0.0
    Product = Cisco Network Security
    Conditions = [ """: %PKI-""" ]
    Fields = ${DLCiscoParsersTemplates.cisco-system-info.Fields} [
      """\d+:\d+:\d+\s+({host}[\w\-.]+)\s"""
  ]


}
```
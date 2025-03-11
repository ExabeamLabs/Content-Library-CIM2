#### Parser Content
```Java
{
Name = cisco-asa-str-app-notification-success-pdt
    ParserVersion = v1.0.0
    Product = Cisco Network Infrastructure and Management
    Conditions = [ """: %ILPOWER-""" ]
    Fields = ${DLCiscoParsersTemplates.cisco-system-info.Fields} [
      """\d+:\d+:\d+\s+({host}[\w\-.]+)"""
    ]
  

}
```
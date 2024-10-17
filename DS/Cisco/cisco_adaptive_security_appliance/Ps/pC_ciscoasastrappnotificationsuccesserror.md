#### Parser Content
```Java
{
Name = cisco-asa-str-app-notification-success-error
    ParserVersion = v1.0.0
    Product = Cisco Adaptive Security Appliance
    Conditions = [ """: %ENTROPY-""" ]
    Fields = ${DLCiscoParsersTemplates.cisco-system-info.Fields} [
      """\d+:\d+:\d+\s+({host}[\w\-.]+)\s"""
    ]
  

}
```
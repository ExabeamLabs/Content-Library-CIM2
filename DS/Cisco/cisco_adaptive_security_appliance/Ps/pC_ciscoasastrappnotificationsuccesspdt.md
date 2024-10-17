#### Parser Content
```Java
{
Name = cisco-asa-str-app-notification-success-pdt
    ParserVersion = v1.0.0
    Product = Cisco Adaptive Security Appliance
    Conditions = [ """: %ILPOWER-""" ]
    Fields = ${DLCiscoParsersTemplates.cisco-system-info.Fields} [
      """\d+:\d+:\d+\s+({host}[\w\-.]+)"""
    ]
  

}
```
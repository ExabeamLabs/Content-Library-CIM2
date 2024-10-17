#### Parser Content
```Java
{
Name = cisco-asa-str-app-notification-success-l2fm
    ParserVersion = v1.0.0
    Product = Cisco Adaptive Security Appliance
    Conditions = [ """: %L2FM-""" ]
    Fields = ${DLCiscoParsersTemplates.cisco-system-info.Fields} [
      """\d+:\d+:\d+\s+({host}[\w\-.]+)\s"""
      """({time}\d{4} \w{3,4}\s\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2})"""
    ]
  

}
```
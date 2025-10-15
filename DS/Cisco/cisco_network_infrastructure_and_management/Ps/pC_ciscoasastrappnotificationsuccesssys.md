#### Parser Content
```Java
{
Name = cisco-asa-str-app-notification-success-sys
    ParserVersion = v1.0.0
    Product = Cisco Network Infrastructure and Management
    Conditions = [ """: %SYS-""" ]
    Fields = ${DLCiscoParsersTemplates.cisco-system-info.Fields} [
      """\d+:\d+:\d+\s+({host}[\w\-.]+)\s"""
      """({host}[\w\.\-]+):\s*(\d+:)?\s*({time}\w\w\w\s*\d+\s*\d\d:\d\d:\d\d\.\d\d\d): %SYS-5"""
    ]
 

}
```
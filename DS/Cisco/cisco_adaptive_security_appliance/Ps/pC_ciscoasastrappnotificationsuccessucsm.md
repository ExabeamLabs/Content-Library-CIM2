#### Parser Content
```Java
{
Name = cisco-asa-str-app-notification-success-ucsm
    ParserVersion = v1.0.0
    Product = Cisco Adaptive Security Appliance
    Conditions = [ """: %UCSM-""" ]
    Fields = ${DLCiscoParsersTemplates.cisco-system-info.Fields} [
      """({time}\d{4} \w{3,4}\s\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2})"""
      """\d+:\d+:\d+\s+({host}[\w\-.]+)\s"""
      ]
  

}
```
#### Parser Content
```Java
{
Name = cisco-asa-str-app-notification-success-swmatm
    ParserVersion = v1.0.0
    Product = Cisco Network Infrastructure and Management
    Conditions = [ """: %SW_MATM-""" ]
    Fields = ${DLCiscoParsersTemplates.cisco-system-info.Fields} [
      """({time}\d{4} \w{3,4}\s\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2})"""
      """\d+:\d+:\d+\s+({host}[\w\-.]+)\s"""
      ]
  

}
```
#### Parser Content
```Java
{
Name = mcafee-nsp-str-app-notification-faultforwarder
  ParserVersion = "v1.0.0"
  Vendor = McAfee
  Product = McAfee Network Security Platform
  TimeFormat = "yyyy-MM-dd HH:mm:ss z"
  Conditions = [ """ SyslogFaultForwarder: """, """Port:""" ]
  Fields = [
    """({alert_name}The link on Port:.*?is (D|d)own)""",
    """SyslogFaultForwarder:[^;]*;\s*({additional_info}[^;]+?)\s*;([^;]*;){2}\s*({host}[^;]+?)\s*;[^;]*;\s*({category}[^;]+?)\s*;[^;]*;[^;]*;\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d \w+)\s*;\s*({action}[^;]+?)\s*;([^;]*;){2}\s*({alert_severity}\w+)""",
  ]


}
```
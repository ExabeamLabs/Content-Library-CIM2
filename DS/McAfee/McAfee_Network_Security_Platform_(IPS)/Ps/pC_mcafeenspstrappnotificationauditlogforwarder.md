#### Parser Content
```Java
{
Name = mcafee-nsp-str-app-notification-auditlogforwarder
  ParserVersion = "v1.0.0"
  Vendor = McAfee
  Product = McAfee Network Security Platform (IPS)
  TimeFormat = "yyyy-MM-dd HH:mm:ss z"
  Conditions = [ """ SyslogAuditLogForwarder: """, """Port:""" ]
  Fields = [
    """SyslogAuditLogForwarder:\s*({event_name}[^;]+?)\s*;\s*({action}[^;]+?)\s*;\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d \w+)\s*;""",
    """Port:\s*([^;]*?)\s*;\s*({user}[^:;]*?)\s*;""",# message_info is removed
  ]


}
```
#### Parser Content
```Java
{
Name = apache-tomcat-str-app-notification-tomcatcatalina
  ParserVersion = v1.0.0
  Vendor = Apache
  Product = Apache Tomcat
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """TOMCAT-CATALINA""" ]
  Fields = [
  """({app}TOMCAT)""",
  """\w+\s*\d\s+\d\d:\d\d:\d\d\s({host}[^\s]+)""",
  """TOMCAT-CATALINA: (\[.+?\]\s){6}\[({event_category}[^]]+)\]\s\[({operation_type}[^]]+)?""",
  """TOMCAT-CATALINA:.+?\[\]\s:\s({action}[^\s]+)""",
  ]
  DupFields = ["host->dest_host"]


}
```
#### Parser Content
```Java
{
Name = infoblox-nios-str-configuration-create-dashboardconfiguration
  Vendor = Infoblox
  Product = Infoblox NIOS
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ httpd: """, """]: Created DashboardConfiguration """ ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """: ({time}\d{4}-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)""",
    """({operation}Created DashboardConfiguration)""",
# dashboard_type is removed
# dashboard_config_name is removed
  ]
  ParserVersion = "v1.0.0"


}
```
#### Parser Content
```Java
{
Name = kemp-loadmaster-str-alert-trigger-success-attempted
  Vendor = Kemp
  Product = Kemp LoadMaster
  TimeFormat = "epoch"
  Conditions = [ """ l7log:""", """ Attempted """, """ attack on """ ]
  Fields = [
    """\s({host}[\w\.\-]+)\s+\S+\s+\S+\s+l7log:""",
    """attack on\s+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\s+from\s+({url}[^\(\s]+)\s+\(({additional_info}.+?)\)""",
    """\sAttempted\s+({alert_name}.+?)\s+on""",
  ]
  DupFields = [ alert_name->alert_type ]
  ParserVersion = "v1.0.0"


}
```
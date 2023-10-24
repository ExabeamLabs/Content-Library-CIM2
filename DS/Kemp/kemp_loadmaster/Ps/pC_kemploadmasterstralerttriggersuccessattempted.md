#### Parser Content
```Java
{
Name = kemp-loadmaster-str-alert-trigger-success-attempted
  Vendor = Kemp
  Product = Kemp LoadMaster
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ l7log:""", """ Attempted """, """ attack on """ ]
  Fields = [
    """\s({host}[\w\.\-]+)\s+\S+\s+\S+\s+l7log:""",
    """attack on\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\s+from\s+({malware_url}[^\(\s]+)\s+\(({additional_info}.+?)\)""",
    """\sAttempted\s+({alert_name}.+?)\s+on""",
  ]
  DupFields = [ alert_name->alert_type ]
  ParserVersion = "v1.0.0"


}
```
#### Parser Content
```Java
{
Name = trendmicro-officescan-kv-alert-trigger-success-logdevicecontrol
  ParserVersion = v1.0.0
  Vendor = Trend Micro
  Product = OfficeScan
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ WFBSS-SVC-AC [LogDeviceControl""" ]
  Fields = [
    """({host}\S+) WFBSS-SVC-AC""",
    """\d+ ({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d) \d+\.\d+\.\d+\.\d+""",
    """Device name="({src_host}[^"]+)""",
    """User="({user}[\w\.\-]{1,40}\$?)""",
    """Subject="({file_path}.+?\\({file_name}[^\\"]+))"""",
    """\[({alert_type}[^@]+)""",
  ]
  DupFields = [ "file_name->alert_name" ]


}
```
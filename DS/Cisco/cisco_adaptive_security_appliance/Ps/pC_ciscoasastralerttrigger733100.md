#### Parser Content
```Java
{
Name = cisco-asa-str-alert-trigger-733100
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-733100""", """%ASA-""" ]
  Fields = [
    """\w+ \d+ \d\d:\d\d:\d\d (::ffff:)?({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}) ({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)""",
    """({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d) (::ffff:)?({host}[\w\-.]+)\s*:\s*%ASA""",
    """%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """%ASA\-\d+\-\d+:\s*\[\s*({object}.+?)\s*\] drop (\S+) ({event_name}exceeded)"""# rate_id is removed
    """Current burst rate is ([\+\-]*\d+) per second, max configured rate is ({max_rate_val_1}[\+\-]*\d+)""",# burst_rate_val is removed
    """Current average rate is ([\+\-]*\d+) per second, max configured rate is ({max_rate_val_2}[\+\-]*\d+)""",# average_rate_val is removed
# total_cnt is removed
  ]
  ParserVersion = "v1.0.0"


}
```
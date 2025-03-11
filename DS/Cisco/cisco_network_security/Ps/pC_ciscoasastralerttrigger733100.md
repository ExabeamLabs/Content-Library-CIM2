#### Parser Content
```Java
{
Name = cisco-asa-str-alert-trigger-733100
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = ["MMM dd yyyy HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """-733100""", """%ASA-""" ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """\w+ \d+ \d\d:\d\d:\d\d (::ffff:)?({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}) ({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)""",
    """({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)( (::ffff:)?({host}[\w\-.]+)\s*)?:\s*%ASA""",
    """%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """%ASA\-\d+\-\d+:\s*\[\s*({object}.+?)\s*\] drop (\S+) ({event_name}exceeded)"""# rate_id is removed
    """Current burst rate is ([\+\-]*\d+) per second, max configured rate is ({max_rate_val_1}[\+\-]*\d+)""",# burst_rate_val is removed
    """Current average rate is ([\+\-]*\d+) per second, max configured rate is ({max_rate_val_2}[\+\-]*\d+)""",# average_rate_val is removed
    """(-|({host}[\w\.-]+))\s*%ASA-|\s+(::ffff:)?({=host}[\w\.-]+)\s*:\s*%ASA-"""
# total_cnt is removed
  ]
  ParserVersion = "v1.0.0"


}
```
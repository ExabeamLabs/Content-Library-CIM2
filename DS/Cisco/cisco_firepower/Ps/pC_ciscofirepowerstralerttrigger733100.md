#### Parser Content
```Java
{
Name = cisco-firepower-str-alert-trigger-733100
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-733100""", """%FTD-""" ]
  Fields = [
    """({time}\d{1,4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}Z?)""",
    """\w+ \d+ \d\d:\d\d:\d\d ({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}) ({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)""",
    """({host}[\w+\.-]+)\s+(\S*:\s*)?%FTD-\d+-\d+:""",
    """({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d) ({host}[\w\-.]+)\s*:\s*%FTD""",
    """%FTD\-({priority}\d+)\-({event_code}\d+)""",
# rate_id is removed
# burst_rate_val is removed
# average_rate_val is removed
# total_cnt is removed
  ]
  ParserVersion = "v1.0.0"


}
```
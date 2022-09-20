#### Parser Content
```Java
{
Name = symantec-endpointprotection-kv-app-activity-category
    ParserVersion = v1.0.0
    Vendor = Symantec
    Product = Symantec Endpoint Protection
    TimeFormat = "YYYY-mm-dd HH:mm:ss"
    Conditions = [ """SymantecServer: """, """,Category: """]
    Fields = [
      """\d\d:\d\d:\d\d\s({host}[^\s]+) SymantecServer:""",
      """time:\s*({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""",
      """SymantecServer:\s*({server}[^,]+)""",
      """Category:\s*({category}[^,]+),({alert_type}[^,]+),"*({additional_info}[^,.]+)""",
      """Remote file path:\s*({file_path}[^,]+)""",
      """DuResult:\s*({result}[^,]+)""",
      """LiveUpdate encountered an error:\s*({failure_reason}[^,]+)""",
      """SONAR encountered an error:\s*({failure_reason}[^,]+)""",
    ]


}
```
#### Parser Content
```Java
{
Name = cisco-fp-str-app-activity-success-609001
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = v1.0.0
  TimeFormat = ["MMM dd yyyy HH:mm:ss","MMM dd HH:mm:ss"]
  Conditions = [ """%FTD-""", """-609001""", """: Built """ ]
  Fields = [
    """({time}\w+ \d+ (\d\d\d\d )?\d\d:\d\d:\d\d)\s(\w+\s)?({host}[\w\-.]+)\s*:\s*(\w+\s|%\w+\-)"""
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """({event_name}Built .+?)\s+$""",
    """(Teardown|Built) local-host ([^\s]+|INSIDE|Outside|outside):(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))($|\s)"""
  ]


}
```
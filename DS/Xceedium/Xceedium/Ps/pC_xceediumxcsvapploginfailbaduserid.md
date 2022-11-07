#### Parser Content
```Java
{
Name = xceedium-x-csv-app-login-fail-baduserid
  Vendor = Xceedium
  Product = Xceedium
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Message 18002:""", """Bad User ID""" ]
  Fields = [
    """"+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"+\s*,""",
    ""","(|[- ]+|({src_ip}\S+?))",((\s*"([^"]|"")+")\s*,|[^",]+?,|\s*,){9}\s*"Message 18002:""",
    """Message 18002:\s*Bad User ID\s*\(\s*({user}.+?)\s*\)""",
    """Message ({http_response_code}\d+)""",
  ]
  DupFields = ["host->dest_host"]
  ParserVersion = v1.0.0


}
```
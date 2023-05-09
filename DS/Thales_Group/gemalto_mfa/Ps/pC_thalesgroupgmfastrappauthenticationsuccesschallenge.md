#### Parser Content
```Java
{
Name = thalesgroup-gmfa-str-app-authentication-success-challenge
  ParserVersion = "v1.0.0"
  Vendor = Thales Group
  Product = Gemalto MFA
  TimeFormat = "MM/d/yyyy H:mm:ss a"
  Conditions = [ """ resulting in CHALLENGE. """ ]
  Fields = [
    """""<\d+>\w+\s+\d+:\d+:\d+\s+({host}\S+)""",
    """At\s+({time}\d+/\d+/\d\d\d\d \d+:\d+:\d+ (am|AM|PM|pm)),\s*({user}[^\s\(]+)\S*\s+from\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+did\s+({action}\S+)""",
    """using\s+({auth_method}\S+)""",
    """resulting in ({result}CHALLENGE)""",
  ]


}
```
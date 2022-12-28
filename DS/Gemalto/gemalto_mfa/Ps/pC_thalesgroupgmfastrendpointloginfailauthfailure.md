#### Parser Content
```Java
{
Name = thalesgroup-gmfa-str-endpoint-login-fail-authfailure
  Vendor = Gemalto
  Product = Gemalto MFA
  TimeFormat = "MM/d/yyyy H:mm:ss a"
  Conditions = [ """ resulting in AUTH_FAILURE. """ ]
  Fields = [
    """""<\d+>\w+\s+\d+:\d+:\d+\s+({host}\S+)""",
    """At\s+({time}\d+/\d+/\d\d\d\d \d+:\d+:\d+ (am|AM|PM|pm)),\s*({user}[^\s\(]+)\S*\s+from\s+({src_ip}[a-fA-F\d.:]+)\s+did\s+({action}\S+)""",
    """using\s+({auth_method}\S+)""",
    """resulting in ({result}AUTH_FAILURE)\.(\s*({failure_reason}.+?))?\s*""""",
  ]
  ParserVersion = "v1.0.0"


}
```
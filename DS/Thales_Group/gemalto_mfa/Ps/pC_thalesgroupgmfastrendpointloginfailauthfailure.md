#### Parser Content
```Java
{
Name = thalesgroup-gmfa-str-endpoint-login-fail-authfailure
  Vendor = Thales Group
  Product = Gemalto MFA
  TimeFormat = "MM/d/yyyy H:mm:ss a"
  Conditions = [ """ resulting in AUTH_FAILURE. """ ]
  Fields = [
    """""<\d+>\w+\s+\d+:\d+:\d+\s+({host}\S+)""",
    """At\s+({time}\d+/\d+/\d\d\d\d \d+:\d+:\d+ (am|AM|PM|pm)),\s*({user}[^\s\(]+)\S*\s+from\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+did\s+({action}\S+)""",
    """using\s+({auth_method}\S+)""",
    """resulting in ({result}AUTH_FAILURE)\.(\s*({failure_reason}.+?))?\s*""""",
  ]
  ParserVersion = "v1.0.0"


}
```
#### Parser Content
```Java
{
Name = symantec-endpointprotection-kv-alert-trigger-success-registryread
  ParserVersion = v1.0.0
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """,Rule:""", """,Registry Read,Begin:""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),({alert_severity}[^,]+),({alert_type}[^,]+),({host}[^,]+),({action}[^,]+),[^,]*,({operation}[^,]+),([^,]*,){2}({alert_name}[^,]+),[^,]*,({file_path}({file_dir}[^,]*?[\\\/]+)?({file_name}[^,\\\/]+?(\.({file_ext}\w+))?)?),""",
    """,User:\s*(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),""",
    """,Domain:\s*({domain}[^,]+),""",
    """,File size \(bytes\):\s*(0|({bytes}\d+)),""",
  ]


}
```
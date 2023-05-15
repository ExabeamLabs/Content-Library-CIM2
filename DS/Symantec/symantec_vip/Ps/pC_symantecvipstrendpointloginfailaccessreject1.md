#### Parser Content
```Java
{
Name = symantec-vip-str-endpoint-login-fail-accessreject-1
  Vendor = Symantec
  Product = Symantec VIP
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS z"
  Conditions = [ """text=Sending Access-Reject for user""" ]
  Fields = [
    """INFO.*?({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\.\d\d\d \w+(\+|\-)\d+)\s*"\s+\S+\s+({service_name}[^":]+)""",
    """for user \[({user}[^\]\s]+)""",
    """reason=[^;]*;\s*({failure_reason}[^"]*?)\.?""""
  ]
  ParserVersion = v1.0.0


}
```
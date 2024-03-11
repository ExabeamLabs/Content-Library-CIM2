#### Parser Content
```Java
{
Name = symantec-vip-kv-endpoint-login-success-authentication
  Vendor = Symantec
  Product = Symantec VIP
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS z"
  Conditions = [ """text=Authentication Success for user""", """StatusMessage: Mobile push request approved by user""" ]
  Fields = [
    """INFO[^~]+({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\.\d\d\d \w+(\+|\-)\d+)\s*"\s+\S+\s+({service_name}[^":]+)""",
    """({event_name}Authentication Success for user)"""
    """for user \[(({domain}[^\\]+)\\)?({user}[^\]\s]+)"""
  ]
  ParserVersion = v1.0.0


}
```
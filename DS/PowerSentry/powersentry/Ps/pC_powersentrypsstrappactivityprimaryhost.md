#### Parser Content
```Java
{
Name = "powersentry-ps-str-app-activity-primaryhost"
Vendor = "PowerSentry"
Product = "PowerSentry"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """ [Sentry"""
  """ primary host changed to """
]
Fields = [
  """\d\d:\d\d:\d\d ({host}[^\s]+) \[({src_host}[^\]]+)\].+? by user "({user}[\w\.\-]{1,40}\$?)"""
  """({operation}primary host changed)"""
]
ParserVersion = "v1.0.0"


}
```
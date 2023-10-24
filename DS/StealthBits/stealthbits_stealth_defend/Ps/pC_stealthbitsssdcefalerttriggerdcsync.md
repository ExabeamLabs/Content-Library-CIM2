#### Parser Content
```Java
{
Name = stealthbits-ssd-cef-alert-trigger-dcsync
  Vendor = StealthBits
  Product = StealthBits Stealth Defend
  TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
  Conditions = [ """CEF:""", """|STEALTHbits Technologies|StealthDEFEND|""", """threatType=DCSync """]
  Fields = [
    """threatTime=({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\dZ)""",
    """computers=([^\\]+\\)?({host}[^;]+)""",
    """threatType=({alert_name}[^=]+)\s+\w+=""",
    """users=(({domain}[^\\]+)\\)?({user}[\w\.\-]{1,40}\$?)""",
  ]
  DupFields = [ "alert_name->alert_type" ]
  ParserVersion = "v1.0.0"


}
```
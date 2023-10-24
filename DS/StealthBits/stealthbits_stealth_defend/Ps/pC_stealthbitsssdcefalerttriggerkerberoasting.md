#### Parser Content
```Java
{
Name = stealthbits-ssd-cef-alert-trigger-kerberoasting
  ParserVersion = v1.0.0
  Vendor = StealthBits
  Product = StealthBits Stealth Defend
  TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
  Conditions = [ """CEF:""", """|STEALTHbits Technologies|StealthDEFEND|""", """threatType=Kerberoasting """]
  Fields = [
    """threatTime=({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\dZ)""",
    """threatType=({alert_name}[^=]+)\s+\w+=""",
    """users=([^\\]+\\)?({user}[\w\.\-]{1,40}\$?)""",
    """computers=([^\\]+\\)?({host}[^;]+)""",
   ]
   DupFields = [ "alert_name->alert_type" ]


}
```
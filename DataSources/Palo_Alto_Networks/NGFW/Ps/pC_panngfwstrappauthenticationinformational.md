#### Parser Content
```Java
{
Name = pan-ngfw-str-app-authentication-informational
  Vendor = Palo Alto Networks
  Product = NGFW
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """,SYSTEM,auth,""", """,general,informational,"""]
  Fields = [
    """({host}[\w\-\.]+)[\s\-]+\d+,({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,SYSTEM,auth,""",
    """Client\s'({src_ip}[A-Fa-f:\d\.]+)""",
    """,SYSTEM,auth,([^,]+,){2

}
```
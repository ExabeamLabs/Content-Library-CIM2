#### Parser Content
```Java
{
Name = pan-ngfw-csv-dhcp-traffic-generalinformational
  ParserVersion = v1.0.0
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy/MM/dd HH:mm:ss"]
  Conditions = [ """,SYSTEM,dhcp,""", """,general,informational,"""]
  Fields = [
    """({host}[\w\-\.]+)[\s\-]+\d+,({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,SYSTEM,dhcp""",
    """,SYSTEM,dhcp,([^,]+,){2

}
```
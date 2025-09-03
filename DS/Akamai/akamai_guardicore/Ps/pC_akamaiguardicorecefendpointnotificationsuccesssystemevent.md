#### Parser Content
```Java
{
Name = akamai-guardicore-cef-endpoint-notification-success-systemevent
    Vendor = Akamai 
    Product = Akamai Guardicore
    TimeFormat = "yyyy-MM-dd'T'HH:mmZ"
    Conditions = [ """CEF:""" , """Guardicore|Centra""", """|System Event|""" ]
    Fields = [
      """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\dZ)""",
      """CEF:\d+\|([^\|]+\|){4}({event_name}[^\|]+)""", 
      """CEF:\d+\|([^\|]+\|){3}({category}[^\|]+)""",
      """CEF:\d+\|([^\|]+\|){5}({severity}[^\|]+)""",
      """msg=({additional_info}[^,]+)"""
    ]
    ParserVersion = v1.0.0
  

}
```
#### Parser Content
```Java
{
Name = akamai-guardicore-cef-endpoint-notification-success-agentlogevent
    Vendor = Akamai 
    Product = Akamai Guardicore
    TimeFormat = "yyyy-MM-dd'T'HH:mmZ"
    Conditions = [ """CEF:""" , """Guardicore|Centra""", """|Agent Log Event|""" ]
    Fields = [
      """start=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\dZ)""",
      """CEF:\d+\|([^\|]+\|){4}({event_name}[^\|]+)""", 
      """CEF:\d+\|([^\|]+\|){3}({category}[^\|]+)""",
      """CEF:\d+\|([^\|]+\|){5}({severity}[^\|]+)""",
      """ip:\s*({dest_ip}[^,]+)""",
      """msg=({additional_info}[^,]+)"""
    ]
    ParserVersion = v1.0.0
  

}
```
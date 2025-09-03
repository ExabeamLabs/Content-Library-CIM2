#### Parser Content
```Java
{
Name = akamai-guardicore-cef-endpoint-notification-success-assetlabelchange
    Vendor = Akamai 
    Product = Akamai Guardicore
    TimeFormat = "yyyy-MM-dd'T'HH:mmZ"
    Conditions = [ """CEF:""" , """Guardicore|Centra""", """|Asset Label Change|""", """New label change entry reported by the Guardicore Security Suite""" ]
    Fields = [
      """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\dZ)""",
      """CEF:\d+\|([^\|]+\|){4}({event_name}[^\|]+)""",
      """CEF:\d+\|([^\|]+\|){3}({category}[^\|]+)""",
      """Asset name:\s*({dest_host}[^,]+)""",
      """IP Addresses:\s*\['({dest_ip}[^,']+)'""",
      """Asset id:\s*({asset_id}[^,]+)""",
      """msg=({additional_info}[^,]+)"""
    ]
    ParserVersion = v1.0.0
  

}
```
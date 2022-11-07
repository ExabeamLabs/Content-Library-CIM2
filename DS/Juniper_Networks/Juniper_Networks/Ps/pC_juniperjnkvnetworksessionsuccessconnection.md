#### Parser Content
```Java
{
Name = juniper-jn-kv-network-session-success-connection
    Vendor = Juniper Networks
    Product = Juniper Networks
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """ PulseSecure: """, """SOURCE_IP=""", """SOURCE_INTERFACE=""" ]
    Fields = [
      """PulseSecure:\s+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+\-\s+({host}\S+)""",
      """SOURCE_IP="({src_ip}[a-fA-F\d.:]+)""",
      """SOURCE_INTERFACE="({src_interface}[^"]+)""",
      """DEST_IP="({dest_ip}[a-fA-F\d.:]+)""",
    ]
    ParserVersion = "v1.0.0"


}
```
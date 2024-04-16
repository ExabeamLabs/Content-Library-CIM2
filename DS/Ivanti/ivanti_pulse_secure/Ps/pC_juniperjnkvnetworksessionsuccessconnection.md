#### Parser Content
```Java
{
Name = juniper-jn-kv-network-session-success-connection
    Vendor = Ivanti
    Product = Ivanti Pulse Secure
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """ PulseSecure: """, """SOURCE_IP=""", """SOURCE_INTERFACE=""" ]
    Fields = [
      """PulseSecure:\s+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s+\-\s+({host}\S+)""",
      """SOURCE_IP="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """SOURCE_INTERFACE="({src_interface}[^"]+)""",
      """DEST_IP="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    ]
    ParserVersion = "v1.0.0"


}
```
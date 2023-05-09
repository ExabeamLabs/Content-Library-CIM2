#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-login-success-startedaovpn
    ParserVersion = v1.0.0
    Vendor = Ivanti
    Product = Ivanti Pulse Secure
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [
      """PulseSecure:"""
      """: Session started for user"""
      """AOVPN"""
      """VPN Tunneling:"""
    ]
    Fields = [
      """\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s\d""",
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)\s({host}[\w\-.]+)\sPulseSecure:""",
      """,\s+hostname\s+({src_host}[\w.\-]+)""",
      """\s(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w.\-]+))\s+PulseSecure:""",
      """\- \[({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]""",
      """with IP(?:v4 address)?\s+({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
      """Session started for user\s+\(({additional_info}[^\)]+)\)\s""",
      """\]\s*({full_name}[^\(]+?)\(AOVPN\)"""
    ]


}
```
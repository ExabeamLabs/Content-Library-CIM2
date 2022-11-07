#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-login-fail-loginfailed
    ParserVersion = v1.0.0
    Vendor = Juniper Networks
    Product = Pulse Secure
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ 
"""Login failed using auth server"""
"""Reason:"""
]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """\w+\s*\d+\s*\d\d:\d\d:\d\d\s*({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-\.]+)))\s*:\s*\(""",
      """\d\d:\d\d:\d\d\s+-\s+\[({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\]\s+(({domain}[^\\]+)\\)?(?:({email_address}[^@]+@[^@(]+)|({user}.+?))\(""",
      """Reason:\s+({failure_reason}[^"]+?)\s*("|$)""",
      """\d\d:\d\d:\d\d\s+({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+)))\s+.*?PulseSecure:""",
      """PulseSecure:\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+)))""",
      """PulseSecure:[^\[]+\[({src_ip}[A-Fa-f.\d:]+)\]\s+([\w\s]+?::)?(({domain}[^\s\\]+)\\+)?(\?|(?:({email_address}[^@\s]+@[^@\s\(]+)|('\+)?(\)|\w{1,5}://[^\(]+|\$\{.+\}\w*|\.|(({=domain}[^\/\(]+)\/+)?(\.|({user}[^\n]+?)))(\=|\')?(\([\d\*]+\))?(\+')?))\(({realm}[^\(]*)?\)\[([^\]]*)\]\s*\-\s*({failure_reason}[^\(]+?)?\s*\("""
      ]
  

}
```
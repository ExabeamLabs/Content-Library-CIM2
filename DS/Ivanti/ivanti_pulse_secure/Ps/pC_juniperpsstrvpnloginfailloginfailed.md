#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-login-fail-loginfailed
    ParserVersion = v1.0.0
    Vendor = Ivanti
    Product = Ivanti Pulse Secure
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ 
"""Login failed using auth server"""
"""Reason:"""
]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """\w+\s*\d+\s*\d\d:\d\d:\d\d\s*({host}(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-\.]+)))\s*:\s*\(""",
      """\d\d:\d\d:\d\d\s+-\s+\[({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+(({domain}[^\\]+)\\)?(?:({email_address}[^@]+@[^@(]+)|({user}.+?))\(""",
      """Reason:\s+({failure_reason}[^"]+?)\s*("|$)""",
      """\d\d:\d\d:\d\d\s+({host}(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-.]+)))\s+.*?PulseSecure:""",
      """PulseSecure:\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({host}(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-.]+)))""",
      """PulseSecure:[^\[]+\[({src_ip}[A-Fa-f.\d:]+)\]\s+([\w\s]+?::)?(({domain}[^\s\\]+)\\+)?(\?|(?:({email_address}[^@\s]+@[^@\s\(]+)|('\+)?(\)|\w{1,5}://[^\(]+|\$\{.+\}\w*|\.|(({=domain}[^\/\(]+)\/+)?(\.|({user}[^\n]+?)))(\=|\')?(\([\d\*]+\))?(\+')?))\(({realm}[^\(]*)?\)\[([^\]]*)\]\s*\-\s*({failure_reason}[^\(]+?)?\s*\("""
      ]
  

}
```
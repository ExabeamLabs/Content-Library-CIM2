#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-login-fail-hostfailed
    ParserVersion = v1.0.0
    Vendor = Ivanti
    Product = Ivanti Pulse Secure
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ 
"""Host Checker policy """
""" failed on host """
]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s-\s""",
      """\stime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """\sfw=({host}(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-\.]+)))""",
      """\- \[(127\.0\.0\.1|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\]\s+(({domain}[^\\\s\(]+)\\)?({user}[^\\\s\(]+)\(({realm}[^\)]+)?\)""",
      """\s({host}(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-.]+)))\s+\S+\s+PulseSecure:""",
      """\s({host}(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-.]+)))\s+(Juniper|PulseSecure):""",
      """PulseSecure:\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({host}(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-.]+)))""",
      """PulseSecure:.*?\[(127\.0\.0\.1|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\]\s+(({domain}[^\\]+)\\)?({user}[^\s]+)\(({realm}[^\)]+)?""",
      """ for user '(({domain}[^\\]+)\\)?({user}.+?)' reason '({failure_reason}[^';]+).*?'""",
      """({failure_reason}Host Checker policy '.+?' failed on host '?(({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^\s]+?))'?)"""
      """({failure_reason}Host Checker policy '.+?' failed on host '(({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}.+?))' .*? for user '.+?')"""
    ]
  

}
```
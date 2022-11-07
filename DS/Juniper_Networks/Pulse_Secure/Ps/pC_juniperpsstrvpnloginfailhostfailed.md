#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-login-fail-hostfailed
    ParserVersion = v1.0.0
    Vendor = Juniper Networks
    Product = Pulse Secure
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ 
"""Host Checker policy """
""" failed on host """
]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s-\s""",
      """\stime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """\sfw=({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-\.]+)))""",
      """\- \[(127\.0\.0\.1|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))\]\s+(({domain}[^\\\s\(]+)\\)?({user}[^\\\s\(]+)\(({realm}[^\)]+)?\)""",
      """\s({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+)))\s+\S+\s+PulseSecure:""",
      """\s({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+)))\s+(Juniper|PulseSecure):""",
      """PulseSecure:\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+)))""",
      """PulseSecure:.*?\[(127\.0\.0\.1|({src_ip}[a-fA-F:\d.]+))\]\s+(({domain}[^\\]+)\\)?({user}[^\s]+)\(({realm}[^\)]+)?""",
      """ for user '(({domain}[^\\]+)\\)?({user}.+?)' reason '({failure_reason}[^';]+).*?'""",
      """({failure_reason}Host Checker policy '.+?' failed on host '?(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^\s]+?))'?)"""
      """({failure_reason}Host Checker policy '.+?' failed on host '(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}.+?))' .*? for user '.+?')"""
    ]
  

}
```
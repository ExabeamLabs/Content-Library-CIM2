#### Parser Content
```Java
{
Name = vmware-esxi-mix-app-activity-sub
  Vendor = VMware
  Product = VMware ESXi
  ParserVersion = v1.0.0
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd'T'HH:mm:ss"]
  Conditions = ["""Originator@6876""", """sub=""" ]
  Fields = [
    """\s?({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)[^\s]+\s+({host}[^\s]+)\s""",
    """action\s*=\s*({action}\S+)""",
# port is removed
    """Resolved endpoint\s*:\s*({additional_info}[^}]+?)\s*action\s=""",
    """ViewManager\s+[^\s]+\s+({additional_info}[^\s]+)""",
    """({additional_info}(POST|CONNECT|BEGIN|GET|PUT|DELETE|HEAD|PATCH|OPTIONS) [^\s]+)""",
    """Originator@6876[^\]]+\]\s*({additional_info}[^\}\}]+?)\s*$"""
    """GetUserInfoInternal\s*\(?(({domain}[^\\]+)[\\]+({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*,\s\w+\)"""
    """subject=\{Name:\s*(({user}[\w\.\-\!\#\^\~]{1,40}\$?);)?.+?\sDomain:({domain}[^\},]+)"""
    """Auth\]: User\s*(({domain}[^\\]+)[\\]+({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*""""
  ]


}
```
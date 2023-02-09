#### Parser Content
```Java
{
Name = juniper-ps-sk4-app-activity-fail-unabletosynctime
  Vendor = Juniper Networks
  Product = Juniper Pulse Secure
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"PulseSecure:"""", """Unable to synchronize time""" ]
  Fields = [
    """"host":"({host}[^"]+)"""",
    """"timestamp":"({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
    """\- \[({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\]\s+(?:Default Network|Root)::(({domain}[^\\\(]+)\\)?(System|({user}[^\(]+))\(({realm}[^\)]+)?\)\[({resource}[^\]]+)?\]""",
    """\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\s+\-\s+({dest_host}[\w\-.]+)""",
    """({additional_info}Unable to synchronize time, either ({failure_reason}NTP server\(s\) are unreachable or provided symmetric key\(s\) are incorrect).)"""
  ]
  ParserVersion = "v1.0.0"


}
```
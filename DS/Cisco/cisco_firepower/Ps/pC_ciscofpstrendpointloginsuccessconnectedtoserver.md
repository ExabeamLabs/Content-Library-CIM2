#### Parser Content
```Java
{
Name = "cisco-fp-str-endpoint-login-success-connectedtoserver"
Vendor = "Cisco"
Product = "Cisco Firepower"
TimeFormat = "epoch_sec"
Conditions = [
"""Original Address="""
"""Active Directory"""
"""connected to server"""
]
Fields = [
"""\s({time}\d{10}).\d+\s"""
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
"""Original Address=({host}[^\s]+)\s"""
"""events\s*({event_name}.*?)\s*$"""
"""connected to server ({dest_host}[^\s]+) \(({dest_ip}.*?)\)\sas ({domain}[^\/]+)\/({user}[\w\.\-]{1,40}\$?)"""
]
ParserVersion = "v1.0.0"


}
```
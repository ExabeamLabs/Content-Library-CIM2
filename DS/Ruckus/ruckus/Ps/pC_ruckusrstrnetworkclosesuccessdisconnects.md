#### Parser Content
```Java
{
Name = ruckus-r-str-network-close-success-disconnects
  Vendor = Ruckus
  Product = Ruckus
  ParserVersion = "v1.0.0"
  Conditions = [ """ disconnects """, """ WLAN[""", """ AP[""", """User[""" ]

exa-syslog-network-connection = {
  Vendor = Ruckus
  Product = Ruckus
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """User\s*\[({user}[\w\.\-]{1,40}\$?)(@({domain}[\w.\-]+))?(@({src_mac}(\w{2}:){5}\w{2}))?\]""",
    """User\s*\[({src_mac}(\w{2}:){5}\w{2})\]""",
    """User\s*\[host\/({src_host}[\w\-]+)(@({src_mac}(\w{2}:){5}\w{2}))?\]""",
    """WLAN\[({ssid}[^\]]+)""",
    """AP\[({wifiap}[^@\]]+)""",
  ]
  DupFields = [ "host->auth_server", "ssid->network", "wifiap->dest_host" 
}
```
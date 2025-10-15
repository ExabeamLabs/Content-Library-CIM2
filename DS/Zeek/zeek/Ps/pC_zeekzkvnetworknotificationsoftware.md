#### Parser Content
```Java
{
Name = zeek-z-kv-network-notification-software
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """/software.log""" ]
  Fields = [
# DL Fields are removed
    """({time}\d{10})\.\d{6}\s*({host}[^\s]+)\s+([^\s]+)\s+([^\s]+)\s+({event_name}[^\s]+)\s+([^\s]+)\s+([^\s]+)\s+({version_minor2}[^\s]+)\s+({version_minor3}[^\s]+)\s+([^\s]+)\s+([^\s]+?)\s*"""
    """({browser}Chrome|Safari|Opera|(?:F|f)irefox|MSIE|Trident)[^\s]*?""",
    """({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin)[^\s]*?""",
	]
  ParserVersion = "v1.0.0"


}
```
#### Parser Content
```Java
{
Name = eset-es-str-app-notification-lognotificationoccurred
  ParserVersion = v1.0.0
  Vendor = ESET
  Product = ESET Endpoint Security
  TimeFormat = "MMM dd, yyyy, hh:mm:ss a"
  Conditions = [ """ESET""", """An Event Log notification has occurred with the following parameters:""" ]
  Fields = [
    """ComputerName =({host}[^|]+)\|""",
    """HardwareDetection=({device_facility}[^|]+)\|""",
    """Notification=({action}.+?)\s*$""",
    """({time}\w+ \d{1,2

}
```
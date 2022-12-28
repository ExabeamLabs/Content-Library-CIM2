#### Parser Content
```Java
{
Name = onespan-dp-kv-endpoint-authentication-success-sourcelocation
  Vendor = OneSpan
  Product = Digipass for Apps
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """Source Location """, """Event:""", """AMID:""" ]
  Fields = [
    """Timestamp:\s({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d)""",
    """Event:\s+\[[^\]]+\]\s({event_name}[^:]+)\.\s\w+:""",
    """User ID\s*:\s*({user}[^\

}
```
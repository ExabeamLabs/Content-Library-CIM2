#### Parser Content
```Java
{
Name = "cisco-ise-str-app-notification-audit"
  Vendor = "Cisco"
  Product = "Cisco Identity and Access Management"
  Conditions = [
    """CISE_MONITORING_DATA_PURGE_AUDIT"""
    """ MESSAGE="""
   ]
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})"""
    """MESSAGE=({additional_info}.+?)$"""
    """({event_name}CISE_MONITORING_DATA_PURGE_AUDIT)"""
    """({event_code}60198)"""
  ]
  ParserVersion = "v1.0.0"


}
```
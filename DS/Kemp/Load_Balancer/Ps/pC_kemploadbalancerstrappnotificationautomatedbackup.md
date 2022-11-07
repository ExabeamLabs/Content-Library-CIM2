#### Parser Content
```Java
{
Name = kemp-loadbalancer-str-app-notification-automatedbackup
  Vendor = Kemp
  Product = Load Balancer
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """logger: """, """Automated Backup to """ ]
  Fields = [
    """logger:\s+({event_name}.+?)\s+$""",
    """User\s+({user}.+?)\s+\(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\)""",
    """({event_category}logger)""",
    """to\s+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s+successful""",
  ]
  ParserVersion = "v1.0.0"


}
```
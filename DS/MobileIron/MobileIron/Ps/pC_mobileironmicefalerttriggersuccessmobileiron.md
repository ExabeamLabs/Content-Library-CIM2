#### Parser Content
```Java
{
Name = mobileiron-mi-cef-alert-trigger-success-mobileiron
  Vendor = MobileIron
  Product = MobileIron
  TimeFormat = "epoch_sec"
  Conditions = [ """CEF:""", """|Mobile Iron|""", """deviceSeverity=""", """dtz=""" ]
  Fields = [
    """ start=({time}\d+) """,
    """ eventId=({alert_id}\d+)""",
    """ cat=({alert_name}[^\s]+) """,
    """ suser=({user}.+?)\s+\w+=""",
    """ act=({action}.+?)\s+\w+=""",
    """ dvc=({host}.+?) """,
    """ agt=({src_ip}.+?) """,
    """ act=({alert_name}.+?)\s+\w+=""",
    """ cat=({alert_type}.+?)\s+\w+=""",
    """ cs1=({additional_info}.+?)\s+\w+=""",
    """ cs3=\{({src_host}.+?)\}\s+\w+=""",
  ]
  ParserVersion = "v1.0.0"


}
```
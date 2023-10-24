#### Parser Content
```Java
{
Name = mobileiron-mi-cef-alert-trigger-success-mobileiron
  Vendor = MobileIron
  Product = MobileIron
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Mobile Iron|""", """deviceSeverity=""", """dtz=""" ]
  Fields = [
    """ start=({time}\d{13}) """,
    """ eventId=({alert_id}\d+)""",
    """ cat=({alert_name}[^\s]+) """,
    """ suser=({user}[\w\.\-]{1,40}\$?)\s+\w+=""",
    """ act=({action}.+?)\s+\w+=""",
    """ dvc=({host}[\w\-.]+) """,
    """ agt=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))? """,
    """ act=({alert_name}.+?)\s+\w+=""",
    """ cat=({alert_type}.+?)\s+\w+=""",
    """ cs1=({additional_info}.+?)\s+\w+=""",
    """ cs3=\{({src_host}[\w\-.]+?)\}\s+\w+=""",
  ]
  ParserVersion = "v1.0.0"


}
```
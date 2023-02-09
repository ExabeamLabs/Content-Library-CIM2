#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-app-activity-success-applicationcontrol
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "ddMMMyyyy HH:mm:ss"
  Conditions = [ """ProductName ="""", """"Application Control"""", """protocol=""", """packets=""" ]
  Fields = [
    """creation_time="({time}\d{1,2}\w{3}\d{4}\s(\d{2}:){2}\d{2})"""",
    """((\d{2}:){2}\d{2}(\+|\-){1,2}\d{1,2}:\d{2})\s+({host}[A-Fa-f0-9.:]+)\s""",
    """ProductName ="({product_name}Application Control)"""",
    """protocol="(Unknown Protocol|Unknown|({protocol}[^"]+))"""",
    """bytes="({bytes}\d+?)"""",
# client_inbound_bytes is removed
# client_outbound_bytes is removed
  ]
  ParserVersion = "v1.0.0"


}
```
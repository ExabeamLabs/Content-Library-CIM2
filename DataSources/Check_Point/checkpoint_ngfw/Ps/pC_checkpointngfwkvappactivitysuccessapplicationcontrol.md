#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-app-activity-success-applicationcontrol
  Vendor = Check Point
  Product = checkpoint ngfw
  TimeFormat = "ddMMMyyyy HH:mm:ss"
  Conditions = [ """ProductName ="""", """"Application Control"""", """protocol=""", """packets=""" ]
  Fields = [
    """creation_time="({time}\d{1,2}\w{3}\d{4}\s(\d{2}:){2}\d{2})"""",
    """((\d{2}:){2}\d{2}(\+|\-){1,2}\d{1,2}:\d{2})\s+({host}[A-Fa-f0-9.:]+)\s""",
    """ProductName ="({product_name}Application Control)"""",
    """protocol="(Unknown Protocol|Unknown|({protocol}[^"]+))"""",
    """bytes="({bytes}\d+?)"""",
    """client_inbound_bytes="({client_inbound_bytes}\d+?)"""",
    """client_outbound_bytes="({client_outbound_bytes}\d+?)""""
  ]
  ParserVersion = "v1.0.0"


}
```
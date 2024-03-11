#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-http-traffic-fail-urlfiltering
  ParserVersion = v1.0.0
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "ddMMMyyyy HH:mm:ss"
  Conditions = [ """ProductName ="""", """"URL Filtering"""" ]
  Fields = [
    """creation_time="({time}\d{1,2}\w{3}\d{4}\s(\d{2}:){2}\d{2})"""",
    """(\d{2}:){2}\d{2}(\+|\-){1,2}\d{1,2}:\d{2}\s+({host}[A-Fa-f0-9.:]+)\s""",
    """ProductName ="({product_name}URL Filtering)"""",
    """protocol="({protocol}[^"]+)"""",
    """user="({user}[^"]+)"""",
    """method="({method}[^"]+)""""
  ]


}
```
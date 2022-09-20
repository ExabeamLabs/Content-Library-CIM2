#### Parser Content
```Java
{
Name = cisco-duo-json-app-activity-success-api
  Vendor = Cisco
  Product = Duo Access Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """API (IAM UI Admin API)""" ]
  Fields = [
    """({time}\d{4}-\d{2}-\d{2}\s(\d{2}:){2}\d{2})""",
    """API \(({app}IAM UI Admin API)\)\|({user}[^\|]+)\|({operation}[^\|]+)\|""",
    """"email":\s*"({email_address}[^@]+@[^.]+\.\w+?)"""",
    """"type":\s*"({object}[^"]+)""""
  ]
  DupFields = ["object->device_name"]
  ParserVersion = "v1.0.0"


}
```
#### Parser Content
```Java
{
Name = "bitdefender-gz-json-app-notification-databsebackup"
  Vendor = "Bitdefender"
  Product = "GravityZone"
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """gravityzone:""", """"name":"Database Backup"""" ]
  Fields = [
    """"created":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)""",
    """"user_name":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
# backup_status is removed
    """"is_successful":({result}[^,]+)""",
    """"location":"({location}[^"]+)""",
  ]


}
```
#### Parser Content
```Java
{
Name = bitdefender-gz-json-app-activity-success-registration
  ParserVersion = "v1.0.0"
  Vendor = Bitdefender
  Product = GravityZone
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","MMM  dd HH:mm:ss"]
  Conditions = [ """gravityzone:""", """"module":"registration"""" ]
  Fields = [
    """({time}\w+\s+\d+\s+\d\d:\d\d:\d\d)""",
    """"computer_name":"({host}[^"]+)""",
    """"user_name":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
# vm_name is removed
# vm_id is removed
# uuid_instance is removed
# uuid_bios is removed
# product_registration is removed
  ]


}
```
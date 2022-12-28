#### Parser Content
```Java
{
Name = bitdefender-gz-json-app-activity-success-registration
  ParserVersion = "v1.0.0"
  Vendor = Bitdefender
  Product = GravityZone
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """gravityzone:""", """"module":"registration"""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """"computer_name":"({host}[^"]+)""",
    """"user_name":"({email_address}[^"]+)""",
# vm_name is removed
# vm_id is removed
# uuid_instance is removed
# uuid_bios is removed
# product_registration is removed
  ]


}
```
#### Parser Content
```Java
{
Name = zeek-z-str-network-notification-x509
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """/x509.log""" ]
  Fields = [
    """({time}\d{10})\.\d{6}\s+"""
#  Dl Fields are removed
  ]
  DupFields = [ "certificate_key_type->auth_method" ]
  ParserVersion = "v1.0.0"


}
```
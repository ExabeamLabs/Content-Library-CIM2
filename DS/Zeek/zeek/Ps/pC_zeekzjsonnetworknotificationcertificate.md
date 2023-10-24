#### Parser Content
```Java
{
Name = zeek-z-json-network-notification-certificate
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """/x509.log""", """"certificate.""" ]
  Fields = [
    """"HOST"+:\s*"+({host}[^"]+)"""",
    """"TAGS"+:\s*"+({event_code}[^"]+)"""",
    """"ts\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
# cert_id is removed
# certificate_version is removed
# certificate_serial is removed
# certificate_subject is removed
# certificate_issuer is removed
# certificate_not_valid_before is removed
# certificate_not_valid_after is removed
# certificate_key_alg is removed
# certificate_sig_alg is removed
# certificate_key_type is removed
# certificate_key_length is removed
# certificate_exponent is removed
# san_dns is removed
# basic_constraints_ca is removed
  ]
  ParserVersion = "v1.0.0"


}
```
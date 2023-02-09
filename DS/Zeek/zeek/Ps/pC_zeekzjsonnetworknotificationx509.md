#### Parser Content
```Java
{
Name = zeek-z-json-network-notification-x509
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """ zeek_x509 """, """"certificate.""" ]
  Fields = [
    """"ts\\?"+:({time}\d{10})""",
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
  ]
  ParserVersion = "v1.0.0"


}
```
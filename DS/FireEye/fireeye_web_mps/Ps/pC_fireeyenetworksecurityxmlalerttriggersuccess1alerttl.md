#### Parser Content
```Java
{
Name = "fireeye-networksecurity-xml-alert-trigger-success-1alert-tl"
    Vendor = "FireEye"
    Product = "FireEye Web MPS"
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [
      ".1.alert:"
      "msg=\"extended\""
      "product=\"web mps"
    ]
    Fields = [
      "(?i)<occurred>({time}\\d\\d\\d\\d-\\d\\d-\\d\\d \\d\\d:\\d\\d:\\d\\d)"
      "(?i)<alert id=\"({alert_id}[^\"]+)"
      "(?i)<malware name=\"({alert_name}[^\"]+)\""
      "(?i)xsi:schemaLocation=.+?name=\"({alert_type}[^\"]+)\".*severity=\"({alert_severity}[^\"]+)\""
    ]
    ParserVersion = "v1.0.0"
  

}
```
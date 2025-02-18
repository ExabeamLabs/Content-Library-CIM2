#### Parser Content
```Java
{
Name = symantec-esc-str-email-spf
    ParserVersion = v1.0.0
    Vendor = Symantec
    Product = Symantec Email Security
    TimeFormat = "epoch_sec"
    Conditions = [
      """|SPF|"""
    ]
    Fields = [
      """\|spf=({spf_result}[^$]+?)$"""
    ]
  

}
```
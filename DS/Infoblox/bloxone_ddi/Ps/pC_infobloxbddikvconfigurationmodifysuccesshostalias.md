#### Parser Content
```Java
{
Name = infoblox-bddi-kv-configuration-modify-success-hostalias
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ httpd: """, """]: Created HostAlias """, """alias=""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s""",
    """: ({time}\d{4}-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)""",
    """({operation}Created HostAlias)""",
# hostalias is removed
# alias is removed
# parent_record is removed
  ]
  ParserVersion = "v1.0.0"


}
```
#### Parser Content
```Java
{
Name = hp-comware-str-app-notification-interface
    ParserVersion = "v1.0.0"
    Vendor = HP
    Product = HPE Comware
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """INTERFACE UPDOWN"""]
    Fields = [
      """Interface\s({interface}\d+)\sis\s({result}[^,]+)""",
      """ifAdminStatus\sis\s({result}\d+)""",
# oper_status is removed
    ]
  

}
```
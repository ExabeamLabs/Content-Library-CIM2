#### Parser Content
```Java
{
Name = securelink-s-str-app-logout-disconnectedfrom
    ParserVersion = "v1.0.0"
    Vendor = SecureLink
    Product = SecureLink
    TimeFormat = "epoch"
    Conditions = [ "SecureLink:","AUDIT:","""disconnected from"""]
    Fields = [
      """Application ({app}[^,\(]+?)\s*(\(|,)""",
      """AUDIT:.+?\(({email_address}[^)]+)\)""",
      """duration ({duration}\w+)""",
    ]
  

}
```
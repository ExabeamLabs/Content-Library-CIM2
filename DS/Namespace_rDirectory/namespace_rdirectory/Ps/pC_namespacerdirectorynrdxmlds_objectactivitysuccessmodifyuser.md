#### Parser Content
```Java
{
Name = namespacerdirectory-nrd-xml-ds_object-activity-success-modifyuser
  ParserVersion = v1.0.0
  Vendor = Namespace rDirectory
  Product = Namespace rDirectory
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """rdirectoryModify User:""", """Modified by:""" ]
  Fields = [
    """SystemTime=\'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)""",
    """Modified by:({user}.+?)\s+(\(.+?\))?\s+\(({domain}[^\/)]+)""",
    """Credentials:({account_domain}[^\\]+)\\+([^\s.]+\.)*({account}[^\s.]+)""",
    """rdirectoryModify.+?\(.+?\)\[({attribute}[^\]]+)""",
    """rdirectoryModify.+?\(.+?\)\[.+?\]\s*Add:({new_attribute}.+?)(\s*To:|<)""",
    """rdirectoryModify.+?\(.+?\)\[.+?\]\s*Change:({old_attribute}.+?)\s*To:""",
    """rdirectoryModify.+?\(.+?\)\[.+?\].+?To:({new_attribute}[^<\[]+)""",
    """rdirectoryModify User:({object}.+?)\s*\("""
  ]


}
```
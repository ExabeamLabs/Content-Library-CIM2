#### Parser Content
```Java
{
Name = namespacerdirectory-nrd-xml-group-member-add-success-memberadd
  ParserVersion = v1.0.0
  Vendor = Namespace rDirectory
  Product = Namespace rDirectory
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """rdirectoryModify Group:""", """Modified by:""", """[Member] Add:""" ]
  Fields = [
    """SystemTime=\'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)""",
    """Modified by:(({user}[\w\.\-]{1,40}\$?)|({full_name}[^",\(]+))\s+(\(.+?\))?\s+\(({domain}[^\/)]+)""",
    """Credentials:({account_domain}[^\\]+)\\+([^\s.]+\.)*({account}[^\s.]+)""",
    """Group:({group_name}.+?)\s+\(({group_domain}[^\/)]+)""",
    """\[Member\]\s*Add:CN=({account_name}[^,]+)""",
    """\[Member\]\s*Add:({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-]+))""",
    """\[Member\]\s*Add:(?:CN|({account_name}[^<]+))"""
  ]


}
```
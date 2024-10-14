#### Parser Content
```Java
{
Name = namespacerdirectory-nrd-xml-user-create-success-createuser
  ParserVersion = v1.0.0
  Vendor = Namespace rDirectory
  Product = Namespace rDirectory
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """rdirectoryCreate User:""", """Modified by:""" ]
  Fields = [
    """SystemTime=\'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)""",
    """Modified by:(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^",\(]+))\s+(\(.+?\))?\s+\(({domain}[^\/)]+)""",
    """User:({account_name}.+?)\s+\(({account_domain}[^\/)]+)"""
    """\[Principal Name\]\s*Add:({account_name}[^@]+)(@({account_domain}[^.]+))?[^\[]*\[""",
    """Credentials:({account_domain}[^\\]+)\\+([^\s.]+\.)*({account}[^\s.]+)""",
    """Add:13=({user_type}\d+)\[Employee Type\]"""
  ]
   DupFields = [ "account_name->dest_user" ]


}
```
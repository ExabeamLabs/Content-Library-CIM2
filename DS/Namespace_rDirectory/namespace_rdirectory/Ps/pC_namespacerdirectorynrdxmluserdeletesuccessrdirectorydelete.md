#### Parser Content
```Java
{
Name = namespacerdirectory-nrd-xml-user-delete-success-rdirectorydelete
  ParserVersion = v1.0.0
  Vendor = Namespace rDirectory
  Product = Namespace rDirectory
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """rdirectoryDelete:""", """Modified by:""" ]
  Fields = [
    """SystemTime=\'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)""",
    """Modified by:({user}.+?)\s+(\(.+?\))?\s+\(({domain}[^\/)]+)""",
    """Credentials:({account_domain}[^\\]+)\\+([^\s.]+\.)*({account}[^\s.]+)""",
    """Delete:\s*({dest_user}.+?)\s+\(({dest_domain}[^\/)]+)"""
  ]
  DupFields = [ "host->dest_host" , "dest_user->account_name"]


}
```
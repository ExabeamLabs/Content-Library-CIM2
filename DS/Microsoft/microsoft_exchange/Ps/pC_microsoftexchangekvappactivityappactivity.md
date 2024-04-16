#### Parser Content
```Java
{
Name = "microsoft-exchange-kv-app-activity-appactivity"
Vendor = "Microsoft"
Product = "Microsoft Exchange"
TimeFormat = "dd/MM/yyyy HH:mm:ss"
Conditions = [
  """Param=""""
  """Identity=""""
  """Cmdlet=""""
]
Fields = [
  """\WUser="({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
  """\WCmdlet="({operation}[^"]+)""""
  """\WServer="({dest_host}[^"]+)""""
  """\WParam="-Identity\s*'({resource}[^'"]+)"""
  """\WParam="-User\s*'({object}[^'"]+)"""
  """\WParam="-OwaMailboxPolicy\s*'({object}[^'"]+)"""
  """\WParam="-DomainController\s*'({object}[^'"]+)"""
  """\WParam="-AccessRights\s*'({object}[^'"]+)"""
  """\WParam="-Server\s*'({object}[^'"]+)"""
  """\WSuccess="({result}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```
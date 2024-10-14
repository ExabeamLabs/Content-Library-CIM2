#### Parser Content
```Java
{
Name = microsoft-mssql-cef-database-delete-success-deletedatabasecommand
Vendor = Microsoft
Product = MSSQL
TimeFormat = "MMM dd yyyy HH:mm:ss z"
Conditions = [
  """CEF:"""
  """|LOGbinder|SQL|"""
  """|24087|Issued a delete database command"""
]
Fields = [
  """({host}[\w.\-]+)\s+CEF:([^\|]*\|){4}({event_code}[^\|]+)\|({event_name}[^\|]+)"""
  """\Wrt=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d \w+)"""
  """\Wduser=(n/a|(({domain}[^=\\\/]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)"""
  """\Wfname=(|({db_name}.+?))(\s+\w+=|\s*$)"""
  """\Wcs1=({db_operation}\w+)"""
  """\WdeviceExternalId=(|({dest_host}.+?))(\s+\w+=|\s*$)"""
]
DupFields = ["event_name->operation"]
ParserVersion = "v1.0.0"


}
```
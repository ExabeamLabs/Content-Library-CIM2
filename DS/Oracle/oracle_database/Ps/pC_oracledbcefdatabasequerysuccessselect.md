#### Parser Content
```Java
{
Name = "oracle-db-cef-database-query-success-select"
Vendor = "Oracle"
Product = "Oracle Database"
TimeFormat = "epoch"
Conditions = [
"""|Oracle|FGA|"""
"""|SELECT|"""
]
Fields = [
"""\|Oracle\|FGA\|([^\|]*\|){2}({db_operation}[^\|]+)"""
"""\WeventId=({event_code}\d+)"""
"""\Wmsg=\s*({db_query}([^\\=]|(\\\\)*\\=|\\)+)\s+(\w+=|$)"""
"""\Wrt=({time}\d{13})"""
"""\Wshost=({src_host}[^\s]+)"""
"""\Wsuser=({user}[\w\.\-]{1,40}\$?)"""
"""\Wdhost=({dest_host}[^\s]+)"""
"""\Wduser=({db_user}[^\s]+)"""
"""\Wcs3=({db_name}[^\s]+)"""
]
DupFields = [
"db_user->account"
]
ParserVersion = "v1.0.0"


}
```
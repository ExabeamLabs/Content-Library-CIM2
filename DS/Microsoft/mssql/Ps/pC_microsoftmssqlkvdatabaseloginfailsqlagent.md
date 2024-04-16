#### Parser Content
```Java
{
Name = microsoft-mssql-kv-database-login-fail-sqlagent
Vendor = "Microsoft"
Product = "MSSQL"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
  """, instance_name="""
  """, account_name="""
  """, client_name="""
  """, application_name="""
]
Fields = [
  """\sinstance_name="({additional_info}[^"]+)"""
  """\saccount_name="(({domain}[^\\\/"]+?)[\\\/]+)?({user}[\w\.\-]{1,40}\$?)\s*""""
  """\sclient_name="({src_host}[^"]+)"""
  """\sapplication_name="({app}[^"]+)"""
  """\sdatabase_name="({db_name}[^"]+)"""
  """\serr_desc="({result}[^"]+)"""
  """\sfirst_login="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)"""
]
ParserVersion = "v1.0.0"


}
```
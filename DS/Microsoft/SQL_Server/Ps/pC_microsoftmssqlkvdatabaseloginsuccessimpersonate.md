#### Parser Content
```Java
{
Name = microsoft-mssql-kv-database-login-success-impersonate
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = SQL Server
  TimeFormat = "epoch"
  Conditions = [ """|Microsoft|SQL Server|""", """|IMPERSONATE|""", """EXECUTE AS LOGIN""" ]
  Fields = [
    """\srt=({time}\d+)""",
    """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdvchost=({host}[^\s]+)""",
    """\sduser=({user}.+?)\s+\w+=""",
    """\sdntdom=({domain}.+?)\s+\w+=""",
    """\sfname=(?:({domain}[^\\]+)\\+)?({account}.+?)\s+\w+=""",
    """\ssourceServiceName =(?: |({service_name}.+?))\s+\w+=""",
    """\scs3=(?: |({db_name}.+?))\s+\w+=""",
    """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdhost=({dest_host}[^\s]+)"""
  ]


}
```
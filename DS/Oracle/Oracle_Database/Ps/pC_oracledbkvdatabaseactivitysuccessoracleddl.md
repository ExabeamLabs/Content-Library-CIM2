#### Parser Content
```Java
{
Name = oracle-db-kv-database-activity-success-oracleddl
  Vendor = Oracle
  Product = Oracle Database
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""oracle-ddl""","""diag_adl""" ]
  Fields = [
    """\d+:\d+:\d+\s({host}[^\s]+)""",
    """diag_adl:(\/\*.+?\*\/\s*)?({additional_info}({db_operation}[^\s]+).+?)\s*$""",
    """TABLE\s*"+({table_name}[^"]+)""",
    """\stable\s*(\s+|({table_name}[^"\s]+))"""
    """database\s*({db_name}[^\s]+)""",
    """DATABASE\s*({db_name}[^\s]+)"""
  ]


}
```
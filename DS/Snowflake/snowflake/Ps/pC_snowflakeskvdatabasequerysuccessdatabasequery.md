#### Parser Content
```Java
{
Name = "snowflake-s-kv-database-query-success-databasequery"
Vendor = "Snowflake"
Product = "Snowflake"
TimeFormat = "epoch_sec"
Conditions = [
"""QUERY_ID=""""
"""QUERY_TEXT=""""
"""QUERY_TYPE=""""
]
Fields = [
"""EPOCH="({time}\d{10})"""
"""USER_NAME="({db_user}[^"]+)""""
"""DATABASE_NAME="({db_name}[^"]+)""""
"""QUERY_ID="({query_id}[^"]+)""""
"""QUERY_TEXT="({db_query}[^"]+?)\s*""""
"""QUERY_TYPE="(UNKNOWN|({db_operation}[^"]+))""""
"""SCHEMA_NAME="({db_schema}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```
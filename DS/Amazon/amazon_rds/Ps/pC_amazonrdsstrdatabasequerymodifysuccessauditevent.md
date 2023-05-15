#### Parser Content
```Java
{
Name = amazon-rds-str-database-query-modify-success-auditevent
  ParserVersion = v1.0.0
  Conditions = [ """]:STATEMENT: """,""""src-account-name":"Amazon RDS"""",""""event-name":"audit-event""""]

amazon-database-operation = {
    Vendor = Amazon
    Product = Amazon RDS
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\s""",
      """(?i)STATEMENT:\s*(DO|({db_query}({db_operation}\w+)[^"]+?))\s*"""",
      """(?i)(INTO|FROM)\s+({table_name}\w+)""",
      """TABLE\s+({table_name}\w+)""",
      """\):({db_user}[^@]+?)@""",
    ]
	DupFields = [ "db_user->user" 
}
```
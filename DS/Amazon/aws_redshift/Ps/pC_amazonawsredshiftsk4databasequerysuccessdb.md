#### Parser Content
```Java
{
Name = amazon-awsredshift-sk4-database-query-success-db
Vendor = Amazon
Product = AWS Redshift
ParserVersion = "v1.0.0"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [ """ Redshift """, """[ db""", """ LOG:""", """pid""", """xid""" ]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)\s[^\s]+\s""",
"""db\\=({db_name}[^=]+?)\s+\w+\\=""",
"""LOG:\s*(|({db_query}.+?))\s*$""",
"""user\\=({db_user}[^=]+?)\s+\w+\\=""",
"""userid\\=({user_id}\d+)"""
]


}
```
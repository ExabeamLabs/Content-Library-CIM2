#### Parser Content
```Java
{
Name = oracle-db-mix-database-query-success-audit
ParserVersion = v1.0.0
Vendor = Oracle
Product = Oracle Database
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Oracle Audit"""
""" ACTION :"""
""" DATABASE USER:"""
"""CLIENT USER:"""
]
Fields = [
"""\Wrt=({time}\d+)"""
"""\Wdvc=({host}[A-Fa-f:\d.]+)"""
"""\Wdvchost=({host}[\w\-.]+)"""
"""({host}[\w\-.]+)\s+Oracle Audit"""
"""ACTION\s+:\[\d+\]\s+'({db_query}({db_operation}\w+)\s*.*?)\s*'\s+DATABASE USER:"""
"""ACTION\s+:\[\d+\]\s+'({db_operation}grant \w+)"""
"""ACTION\s+:\[\d+\]\s+'({db_operation}revoke \w+)"""
"""ACTION\s+:\[\d+\]\s+'({db_operation}alter \w+)"""
"""\sCLIENT USER:\[\d+\]\s*'({user}[^']+)'"""
"""\sDBID:\[\d+\]\s*'(|({db_name}[^']+))'"""
"""\sDATABASE USER:\[\d+\]\s*'(\/|({account}[^'\\/\s]+))'"""
"""\sPRIVILEGE:\[\d+\]\s*'({privilege}[^']+)'"""
]
DupFields = [
"account->db_user"
]


}
```
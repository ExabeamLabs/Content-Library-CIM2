#### Parser Content
```Java
{
Name = oracle-db-mix-database-query-success-audit
ParserVersion = v1.0.0
Vendor = Oracle
Product = Oracle Database
TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"]
Conditions = [
"""Oracle Audit"""
""" ACTION :"""
""" DATABASE USER:"""
"""CLIENT USER:"""
]
Fields = [
"""({time}\w+\s+\d+ \d+:\d+:\d+)"""
"""\Wrt=({time}\d+)"""
"""\Wdvc=({host}[A-Fa-f:\d.]+)"""
"""\Wdvchost=({host}[\w\-.]+)"""
"""\d\d:\d\d:\d\d ({host}[\w\-.]+).+?Oracle Audit"""
"""ACTION\s+:\[\d+\]\s+'({db_query}({db_operation}\w+)\s*.*?)\s*'\s+DATABASE USER:"""
"""ACTION NUMBER:\[\d+\]\s+'({db_operation}\d{1,3})'"?,"""
"""ACTION\s+:\[\d+\]\s+'({db_operation}grant \w+)"""
"""ACTION\s+:\[\d+\]\s+'({db_operation}revoke \w+)"""
"""ACTION\s+:\[\d+\]\s+'({db_operation}alter \w+)"""
"""\sCLIENT USER:\[\d+\]\s*'({user}[\w\.\-\!\#\^\~]{1,40}\$?)'"""
"""\sDBID:\[\d+\]\s*'(|({db_id}[^']+))'"""
"""\sDATABASE USER:\[\d+\]\s*'(\/|({db_user}({account}[^'\\/\s]+)))'"""
"""\sPRIVILEGE\s*:\[\d+\]\s*'({privileges}[^']+)'"""
"""(?i:((create|drop) user))\s+({dest_user}[^\s]+)"""
]


}
```
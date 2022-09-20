#### Parser Content
```Java
{
Name = ibm-guardium-leef-database-query-success-sql-1
  ParserVersion = v1.0.0
  Vendor = IBM
  Product = Guardium
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
"""LEEF:"""
"""|IBM|Guardium|"""
"""|type="""
"""|serverType="""
]
  Fields = [
    """\d\d:\d\d:\d\d ({host}[\w\-.]+) guard_sender""",
    """\|devTime=({time}\d\d\d\d-\d+-\d+ \d\d:\d\d:\d\d)""",
    """\|ruleDesc=({rule_description}[^\|]+)""",
    """\|serverType=({server_type}[^\|]+)""",
    """\|dbUser=(({domain}[^\|\\]+)\\)?({db_user}[^\|\\]+)""",
    """\|usrName =(|({user}[^\|]+))""",
    """\|sourceProgram=({src_program}[^\|]+)""",
    """\|dst=({dest_ip}[a-fA-F\d:.]+)""",
    """\|dstPort=({dest_port}\d+)""",
    """\|src=({src_ip}[a-fA-F\d:.]+)""",
    """\|srcPort=({src_port}\d+)""",
    """\|sql=\s*({db_operation}[^\|]+?)\s*\|""",
    """\|protocol=({protocol}[^\|]+)""",
    """\|usrName =({service_name}[^;\|]+?)\s*(;|\|)"""
  ]
  DupFields = [ "db_user->account" ]


}
```
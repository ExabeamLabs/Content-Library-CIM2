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
    """\|dbUser=(({domain}[^\|\\]+)\\)?({account}({db_user}[^\|\\]+))""",
    """\|usrName =(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """\|sourceProgram=({src_interface}[^\|]+)""",
    """\|dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\|dstPort=({dest_port}\d+)""",
    """\|src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\|srcPort=({src_port}\d+)""",
    """\|sql=\s*({db_operation}[^\|\s]+)""",
    """\|protocol=({protocol}[^\|]+)""",
    """\|usrName =({service_name}[^;\|]+?)\s*(;|\|)"""
    """\WdbName =({db_name}[^\|]+)"""
    """\Wsql=\s*({db_query}[^\|]+?)\s*\|"""
  ]


}
```
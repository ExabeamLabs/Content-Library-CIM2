#### Parser Content
```Java
{
Name = ibm-guardium-leef-database-login-fail-loginfailed
  ParserVersion = v1.0.0
  Vendor = IBM
  Product = Guardium
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
"""LEEF:"""
"""|IBM|Guardium|"""
"""|type=LOGIN_FAILED|"""
]
  Fields = [
    """\d\d:\d\d:\d\d ({host}[\w\-.]+) GuardiumSniffer\[\d+\]""",
    """\d\d:\d\d:\d\d ({host}[\w\-.]+) guard_sender""",
    """\WruleDesc=({rule_description}[^\|]+)""",
    """\WdevTime=({time}\d\d\d\d-\d+-\d+ \d\d:\d\d:\d\d)""",
    """\WserverType=({server_type}[^\|]+)""",
    """\WdbUser=(({domain}[^\|\\]+)\\)?(\?|({db_user}[^\|\\]+))""",
    """\WusrName =(|({user}[^\|]+))""",
    """\WsourceProgram=({src_program}[^\|]+)""",
    """\Wdst=({dest_ip}[^\|]+)""",
    """\WdstPort=({dest_port}\d+)""",
    """\WdbName =(|({db_name}[^\|]+))""",
    """\Wsrc=({src_ip}[^\|]+)""",
    """\WsrcPort=({src_port}\d+)""",
    """\Werror=({failure_reason}[^\|]+?)("|\s*$)"""
  ]
  DupFields = [ "db_user->account" ]


}
```
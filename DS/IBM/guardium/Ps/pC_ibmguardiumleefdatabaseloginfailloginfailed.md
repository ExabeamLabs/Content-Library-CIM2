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
    """\WdbUser=(({domain}[^\|\\]+)\\)?(\?|({account}({db_user}[^\|\\]+)))""",
    """\WusrName =(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """\WsourceProgram=({src_interface}[^\|]+)""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\WdstPort=({dest_port}\d+)""",
    """\WdbName =(|({db_name}[^\|]+))""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\WsrcPort=({src_port}\d+)""",
    """\Werror=({result_reason}[^\|]+?)("|\s*$)"""
  ]


}
```
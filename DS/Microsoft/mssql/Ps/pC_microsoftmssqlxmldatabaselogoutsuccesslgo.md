#### Parser Content
```Java
{
Name = microsoft-mssql-xml-database-logout-success-lgo
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = MSSQL
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """action_id:LGO""", """event_time:""", """session_id:""", """server_principal_id:""" ]
  Fields=[
    """\Wevent_time:({time}\d+\-\d+\-\d+ \d+:\d+:\d+\.\d{3})""",
    """\WUser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|\s*$)""",
    """\WSid=({user_sid}[^\s]+?)(\s+\w+=|\s*$)""",
    """\Wserver_principal_name:(({domain}[^\\\/]+?)[\\\/])?({db_user}[^\\\/\s]+?)(\s+\w+:|\s*$)""",
    """\Wserver_principal_sid:({db_user_sid}[^\s]+)""",
    """\Wserver_instance_name:({dest_host}[\w\-.]+)""",
    """\Wdatabase_name:({db_name}[^\s]+)""",
    """<Level>({run_level}[^<]+)<"""
   ]


}
```
#### Parser Content
```Java
{
Name = microsoft-mssql-xml-database-login-success-33205
  ParserVersion = v1.0.0
  Conditions = [
""">33205</EventID>""",
"""action_id:LGIS"""
  ]

s-mssql-database-login = {
  Vendor = Microsoft
  Product = SQL Server
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Fields = [
    """\WComputerName =({host}[^=\s]+)""",
    """\WEventCode=({event_code}\d+)""",
    """\WSourceName =({service_name}.+?)(\s+\w+=|\s*$)""",
    """\Wsucceeded:({result}[^:\s]+)""",
    """\Wevent_time:({time}\d+\-\d+\-\d+ \d+:\d+:\d+\.\d{3})""",
    """\WUser=({user}[^\s]+?)(\s+\w+=|\s*$)""",
    """\WSid=({user_sid}[^\s]+?)(\s+\w+=|\s*$)""",
    """\Wserver_principal_name:(({domain}[^\\\/]+?)[\\\/])?({db_user}[^\\\/\s]+?)(\s+\w+:|\s*$)""",
    """\Wserver_principal_sid:({db_user_sid}[^\s]+)""",
    """\Wserver_instance_name:({dest_host}[^\s]+)""",
    """\Wadditional_information:.*?<address>({src_ip}[a-fA-F\d.:]+)""",
    """\Wdatabase_name:({db_name}[^\s]+)""",
    """\Wstatement:({failure_reason}[^.]+)"""
  ]
 },

  cef-defender-atp-2 = {
     Vendor = Microsoft
     Product = Defender ATP
     TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
     Fields = [
       """time"+:\s*"+({time}[^"]+)"""",
       """operationName"+:\s*"+({operation}[^"]+)""",
       """category"+:\s*"+({category}[^"]+)""",
       """RemotePort"+:({dest_port}\d+)""",
       """RemoteIP"+:\s*"+({dest_ip}[^"]+)""",
       """"Protocol"+:\s*"+({protocol}[^"]+)""",
       """LocalIP"+:\s*"+({src_ip}[^"]+)""",
       """LocalPort"+:({src_port}\d+)""",
       """ActionType"+:\s*"+({action}[^"]+)""",
       """RemoteIPType"+:\s*"+(null|({direction}[^"]+))""",
       """DeviceName"+:\s*"+({dest_host}[^"]+)""",
       """InitiatingProcessAccountName"+:\s*"+((?i)SYSTEM|(?i)network service|({user}[^"]+))""",
       """"ProcessIntegrityLevel"+:\s*"+({process_integrity}[^"]+)""",
       """InitiatingProcessAccountSid"+:\s*"+({user_sid}[^"]+)""",
       """"InitiatingProcessFolderPath":\s*"({process_path}(({process_dir}[^"]+?)\\+)?({process_name}[^"\\]+))""""
       """InitiatingProcessFileName"+:\s*"+({process_name}[^"]+)""",
     ]
     DupFields = ["category->event_name"
}
```
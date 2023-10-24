#### Parser Content
```Java
{
Name = "imperva-securesphere-kv-database-query-success-query"
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = ["dd MMM yyyy HH:mm:ss","dd MMMM yyyy HH:mm:ss"]
Conditions = [
"""IMPERVA-Imperva"""
""",respSize="""
""",eventType=Query"""
]
Fields = [
"""\WsrcPort=({src_port}\d+)"""
"""\WsrcIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\WdstPort=({dest_port}\d+)"""
"""\WdstIP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\WcreatTime=({time}\d+ \w+ \d\d\d\d \d\d:\d\d:\d\d)"""
"""\WsrvGroup=(|({server_group}[^,]+)),"""
"""\Wservice=(|({service_name}.+?))(,\w+=|\s*$)"""
"""\WappName =(|({app}[^,]+)),"""
"""\WdbUsername=(?:Hashed User \(Unsupported SSL cipher\)|(({domain}[^\\,]+)\\)?({db_user}[^,\\]+?))(,\w+=|\s*$)"""
"""\WdbName =(|({db_name}.+?))(,\w+=|\s*$)"""
"""\WrespSize=({response_size}\d+)"""
"""\Waction=".*?({db_operation}(?i)(insert|delete|truncate|drop|alter|create|update|enable|disable|merge|delete|merge|select|dbcc))"""
"""\WrawQuery="(|({db_query}[^"]+))""""
"""\WeventType=(|({event_category}[^,]+)),"""
"""\WosUsername=(|({user}[\w\.\-]{1,40}\$?)),"""
"""\WsrcHost=(|({src_host}[^,]+)),"""
"""\WsqlError=(|({sql_error}[^,]+)),"""
"""\WrespTime=(({response_size}[^,]+)),"""
"""\WschemaName =(|({db_schema}[^,]+)),"""
]
DupFields = [
"db_user->account"
"user->user"
]
ParserVersion = "v1.0.0"


}
```
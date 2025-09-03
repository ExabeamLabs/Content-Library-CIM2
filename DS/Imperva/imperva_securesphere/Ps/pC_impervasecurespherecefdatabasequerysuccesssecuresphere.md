#### Parser Content
```Java
{
Name = "imperva-securesphere-cef-database-query-success-securesphere"
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""CEF:"""
"""|Imperva Inc.|SecureSphere|"""
"""responseSize="""
"""bindVar=""""
]
Fields = [
"""\d\d:\d\d:\d\d ({host}\S+) CEF:"""
"""\WcreateTime="({time}\w{3} \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wsrc=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
"""\WOperationType="table"[^=]+object="(|({table_name}[^"]+))""""
"""\Wobject="(|({table_name}[^"]+))[^"]+OperationType="table""""
"""\WdbUsername="(|({domain}[^"\\]+)\\)?(|({db_user}[^"\\]+))""""
"""\WserviceName ="(|({service_name}[^"]+))""""
"""\WappName ="(|({app}[^"]+))""""
"""\WosUser="\s*(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
"""\WsrcHost="(|({domain}[^"\\]+)\\)?(|({src_host}[\w\-.]+))""""
"""\WdatabaseName ="(|({db_name}[^"]+))""""
"""\WresponseSize=({response_size}\d+)"""
"""\Woperation="(|(?i)(Logout)|({db_operation}[^"]+))""""
"""\WschemaName ="(|({db_schema}[^"]+))""""
"""\WparsedQuery="(|(N\/A \(logout\))|({db_query}[^\n]+)?)"\s*$"""
]
DupFields = [
"db_user->account"
]
ParserVersion = "v1.0.0"


}
```
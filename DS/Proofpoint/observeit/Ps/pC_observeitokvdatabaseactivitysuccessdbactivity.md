#### Parser Content
```Java
{
Name = "observeit-o-kv-database-activity-success-dbactivity"
Vendor = "Proofpoint"
Product = "ObserveIT"
TimeFormat = "MM/dd/yyyy HH:mm:ss"
Conditions = [
"""EventName =ObserveIT-DBA_Activity;"""
]
Fields = [
"""({host}\S+)\s+(\S+\s+){4}EventName ="""
"""\sStartTime=({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d)"""
"""\sOS=({os}[^;]+?)\s*(;|"*\s*$)"""
"""\sSessionID=({session_id}[^;]+?)\s*(;|"*\s*$)"""
"""\sServerName =({dest_host}[^;]+?)\s*(;|"*\s*$)"""
"""\sDomainName =({domain}[^;]+?)\s*(;|"*\s*$)"""
"""\s(?i)ViewerURL=({additional_info}[^;]+?)\s*(;|"*\s*$)"""
"""\sUserName =(?:n\/a|({user}[^;]+?))\s*(;|"*\s*$)"""
"""\sLoginName =({user}[^;]+?)\s*(;|"*\s*$)"""
"""\sSqlDBName =({db_name}[^;]+?)\s*(;|"*\s*$)"""
"""\sSqlUserName =([^;\\]+\\)?({db_user}[^;]+?)\s*(;|"*\s*$)"""
"""\sClientName =(?:\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({src_host}[^;]+?))\s*(;|"*\s*$)"""
"""\sClientAddress=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sProcessName =({process_name}[^;]+?)\s*(;|"*\s*$)"""
"""\sWindowTitle=({db_object}[^;\-]+?)\s*\-[^;]*?\-\s*({app}[^;\-]+?)\s*;"""
]
DupFields = [
"user -> os_user"
"process_name->service_name"
]
ParserVersion = "v1.0.0"


}
```
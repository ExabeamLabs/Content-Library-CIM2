#### Parser Content
```Java
{
Name = "oracle-db-cef-database-login-success-logon"
Vendor = "Oracle"
Product = "Oracle Database"
TimeFormat = "epoch"
Conditions = [
"""|ORACLE|Oracle|"""
"""|LOGON|"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\sdvc=({host}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-\.]+)))"""
"""\sdvchost=({host}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-\.]+)))"""
"""\seventId=({event_code}\d+)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sdhost=({src_host}[^\s]+)"""
"""\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
"""\sduser=(\/|({account}.+?))\s+\w+="""
"""Oracle Audit.+?OS$USERID:\[\d+\]\s*("|')({user}[\w\.\-\!\#\^\~]{1,40}\$?)("|')"""
"""Oracle Audit.+?\sUSERID:\[\d+\]\s*("|')({account}\d+)"""
"""Oracle Audit.+?DBID:\[\d+\]\s*("|')({db_name}\d+)"""
]
DupFields = [
"account->db_user"
"db_name->db_id"
]
ParserVersion = "v1.0.0"


}
```
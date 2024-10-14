#### Parser Content
```Java
{
Name = "observeit-o-kv-app-login-auditlogins"
Vendor = "Proofpoint"
Product = "ObserveIT"
TimeFormat = "MM/dd/yyyy HH:mm:ss"
Conditions = [
"""EventName =Audit_logins;"""
"""; AuditTime="""
]
Fields = [
"""({host}\S+)\s+(\S+\s+){4}EventName ="""
"""\sAuditTime=({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d)"""
"""\sOS=({os}[^;]+?)\s*(;|"*\s*$)"""
"""\sDomainName =({domain}[^;]+?)\s*(;|"*\s*$)"""
"""\sConsoleUser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*(;|"*\s*$)"""
"""\sClientAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sLoginStatus=({result}[^;]+?)\s*(;|"*\s*$)"""
"""\sLoginStatusDescrition=({failure_reason}[^;]+?)\s*(;|"*\s*$)"""
]
ParserVersion = "v1.0.0"


}
```
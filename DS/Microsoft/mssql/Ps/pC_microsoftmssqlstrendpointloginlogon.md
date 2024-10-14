#### Parser Content
```Java
{
Name = microsoft-mssql-str-endpoint-login-logon
 Vendor = Microsoft
 Product = MSSQL
 TimeFormat = "yyyy-MM-dd HH:mm:ss"
 Conditions = [ """Logon """, """ [CLIENT: """, """ Login """, """ for user '""" ]
 Fields = [
   """({time}\d{4}-\d{1,2}-\d{1,2} \d{1,2}:\d{1,2}:\d{1,2})(\.\d{1,2})?\s+Logon"""
   """({operation}Logon)"""
   """Login\s+({result}[^\s]+)"""
   """Reason:\s({failure_reason}[^\[]+)\s\["""
   """for user '(((NT \w+|({domain}[^\\']+))\\+)?(ANONYMOUS LOGON|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'"""
   """\[CLIENT:\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\]"""
   """Logon\s+({event_name}[^']+?)\s*'"""
 ]
 ParserVersion = "v1.0.0"


}
```
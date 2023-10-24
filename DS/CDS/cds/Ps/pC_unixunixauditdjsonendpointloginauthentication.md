#### Parser Content
```Java
{
Name = "unix-unixauditd-json-endpoint-login-authentication"
Conditions = [
"""audit_id"""
"""PAM:authentication"""
]
ParserVersion = "v1.0.0"

cds-user-activity = {
     Vendor = CDS
     TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
     Fields = [
       """exe="({process_path}[^"]*)"""",
       """\suid=({user_id}[^\s]*)\s""",
       """\stype=({operation_type}[^\s]*)\s""",
       """\d\d:\d\d:\d\d(\.\S+)?\s({host}[^\s]+)\s""",
       """\sexe="({process_dir}.+\/)({process_name}.+?)"""",
       """\spid=({process_id}[^\s]+)\s""",
       """\sauid=({account_id}[^\s]+)\s"""
       """addr=({dest_host}[^\s]+)\s""",
       """acct="({account}[^"]+)"""",
       """res=({result}failed|success)"""
     
}
```
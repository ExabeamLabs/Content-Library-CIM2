#### Parser Content
```Java
{
Name = apache-cassandra-kv-database-login-success-auth
Conditions = [
  """|category:AUTH|"""
  """|type:LOGIN|"""
  """|authenticated:"""
  """|user:"""
  """|operation:"""
]
ParserVersion = "v1.0.0"

mastersam-pam-events = {
  Vendor = MasterSAM
  Product = MasterSAM PAM
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Fields = [
    """({host}[\w\-.]+)\s+Event Time:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)""",
    """\WUser:\s*(({domain}[^\\\s]+)\\+)?({user}[^\\\s]+)""",
    """\Wname=({dest_host}[\w\-.]+)\s+(\w+=|$)""",
    """\Whost=({dest_ip}[A-Fa-f:\d.]+)""",
    """\Wprotocol=({protocol}.+?)\s+(\w+=|$)""",
    """\Wstatus=({result}.+?)\s+(\w+=|$)""",
    """\Wfailed_message=({failure_reason}.+?)\s+(\w+=|$)""",
    """\WActivity:\s*({operation}.+?)\s+User:""",
  
}
```
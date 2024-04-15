#### Parser Content
```Java
{
Name = "unix-unix-kv-endpoint-login-fail-ruser"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""authentication failure;"""
"""logname="""
"""ruser"""
]
Fields = [
"""\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s"""
"""\s({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2})\S+\s+(::ffff:)?({host}[^\s]+)\s+({process_name}[^\s]+)\s+({process_id}\d+)\s"""
"""({host}[\w\.\-]+)?:?\s*sudo:"""
"""ruser=({user}[^\s]+)"""
"""\suser=({user}[^\s\"]+)(\s|\"|$)"""
"""rhost=({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9]+:[A-Fa-f0-9:]+))""",
"""({failure_reason}authentication ({result}failure))"""
"""\suid=({user_id}[^\s]+)\s"""
"""({event_code}ssh)"""
]
ParserVersion = "v1.0.0"


}
```
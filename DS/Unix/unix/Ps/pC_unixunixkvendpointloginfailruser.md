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
"""(::ffff:)?({host}[\w\-.]+)\s+pam_unix"""
"""\w{3}\s\d{1,2}\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s"""
"""\s({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2})\S+\s+(::ffff:)?({host}[^\s]+)\s+({process_name}[^\s]+)\s+({process_id}\d+)\s"""
"""({host}[\w\.\-]+)?:?\s*sudo:"""
"""ruser=((NT AUTHORITY|({domain}\S+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?)|({user}[\w\.\-]{1,40}\$?)))(\s+\w+=|\s*$)"""
"""\suser=((NT AUTHORITY|({domain}\S+))[\\\/]+)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))(\s|\"|$)"""
"""rhost=({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9]+:[A-Fa-f0-9:]+))""",
"""({failure_reason}authentication ({result}failure))"""
"""\suid=({user_id}[^\s]+)\s"""
"""({event_code}ssh)"""
"""\(({auth_method}[^:]+):auth"""
]
ParserVersion = "v1.0.0"


}
```
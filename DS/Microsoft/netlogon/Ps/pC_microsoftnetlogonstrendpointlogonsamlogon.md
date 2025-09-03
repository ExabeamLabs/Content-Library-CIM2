#### Parser Content
```Java
{
Name = microsoft-netlogon-str-endpoint-logon-samlogon
 Vendor = Microsoft
 Product = NetLogon
 TimeFormat = """MM/dd HH:mm:ss"""
 Conditions = [ """[LOGON]""", """Returns""", """SamLogon:""" ]
 ParserVersion = v1.0.0
 Fields = [
 """({time}\d\d\/\d\d\s+\d\d:\d\d:\d\d)\s+""",
 """logon\s+of\s+(ROOT|\(null\)|(({domain}[^\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s"""
 """\(null\)\\({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s\|]+)\s"""
 """from\s+(\(null\)|({src_host}\S+))\s+"""
 """SamLogon:\s+({auth_method}.+?)\s+of""",
 """Returns\s+({result_code}\S+)""",
 """(?:\\)({domain}[^\\]+)(?:\\)({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+from"""
"""\(via\s+({dest_host}[^\)]+)\)""",
]  
 

}
```
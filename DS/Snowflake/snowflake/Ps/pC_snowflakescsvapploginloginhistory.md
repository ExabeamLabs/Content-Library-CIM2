#### Parser Content
```Java
{
Name = "snowflake-s-csv-app-login-loginhistory"
Vendor = "Snowflake"
Product = "Snowflake"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""TEXTUAL_COL""""
""",LOGIN,"""
"""EVENT_TS_"""
]
Fields = [
""",({operation}LOGIN),({user}[\w\.\-]{1,40}\$?),({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),({client_type}[^,]+),({client_version}[^,]+),({login_method}[^,]+),(|[^,]+),({result}[^,]+),(|({failure_code}[^,]+)),(|({failure_reason}[^,]+)),"""
""""EVENT_TS_UTC":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""""
]
ParserVersion = "v1.0.0"


}
```
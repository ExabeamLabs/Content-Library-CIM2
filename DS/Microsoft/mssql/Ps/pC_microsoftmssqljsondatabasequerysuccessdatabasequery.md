#### Parser Content
```Java
{
Name = "microsoft-mssql-json-database-query-success-databasequery"
Vendor = "Microsoft"
Product = "MSSQL"
TimeFormat = ["yyyy-MM-dd HH:mm:ss.SSS", "yyyy-MM-dd HH:mm:ss.SS"]
Conditions = [
"""HostName ="""
"""DatabaseName ="""
"""SessionLoginName ="""
"""EventClass="""
""", TextData="""
]
Fields = [
"""HostName ="+({host}[^"]+)"""
"""StartTime="+({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d+)"""
"""DatabaseName ="+({db_name}[^"]+)"""
"""SessionLoginName ="+(({domain}[^"]+?)\\+({user}[\w\.\-]{1,40}\$?)|({db_user}[^"]+))"""
"""NTDomainName ="+({domain}[^"]+)"""
"""TextData="+({db_query}.+?)\s*""""
"""EventClass="+({event_code}\d+)"""
"""TextData.+?({db_operation}UPDATE|REMOVE|INSERT|ADD_USER|DELETE)"""
"""ApplicationName ="+({app}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```
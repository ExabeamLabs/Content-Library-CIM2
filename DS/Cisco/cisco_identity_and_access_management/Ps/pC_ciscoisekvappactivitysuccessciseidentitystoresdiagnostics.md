#### Parser Content
```Java
{
Name = cisco-ise-kv-app-activity-success-ciseidentitystoresdiagnostics
  Vendor = Cisco
  Product = Cisco Identity and Access Management
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS Z"
  Conditions = [ """CISE_Identity_Stores_Diagnostics""" ]
  Fields = [ 
    """\:\d+\s+({host}[\w\-\.]+)\s+""",
    """({time}\d\d\d\d\-\d\d\-\d\d\s\d\d\:\d\d:\d\d.\d+\s[+-]\d\d:\d\d)""",
    """({event_name}CISE_Identity_Stores_Diagnostics)""",
    """\sUserName =(({domain}[^=]+?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """External-Active-Directory:\s*({additional_info}[^,]+),"""
    """AuthenticationMethod=({auth_method}[^,]+),""",
    """Response=\{QueryResult=({result}[^;\s]*)""",
    """AcsSessionID=({acs_session_id}[^,]+),""",
    """Protocol=({protocol}[^,]+),"""
    """\sCPMSessionID=({session_id}[^,]+)"""
    """\sSelectedAccessService=({dest_service_name}[^,]*)"""
  ]


}
```
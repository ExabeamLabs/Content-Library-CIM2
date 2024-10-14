#### Parser Content
```Java
{
Name = beyondtrust-bi-cef-app-activity-success-appauditdelete
  ParserVersion = v1.0.0
  Vendor = BeyondTrust
  Product = BeyondInsight
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF:""", """act=Delete""", """|BeyondTrust|BeyondInsight|""", """fileType=""", """|AppAudit|Delete|""" ]
  Fields = [
    """start=({time}\w{3,4}\s\d{1,2}\s\d{4}\s\d{1,2}:\d{1,2}:\d{1,2})""",
    """\w+\s\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2}\s({host}[\w\-.]+)""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """act=({operation}[^\s]+)""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """BeyondTrustBeyondInsightEventSeverity=({severity}[^\s]+)""",
    """({app}BeyondInsight)""",
    """fileType=({additional_info}[^=]+?)\s\w+=""",
  ]


}
```
#### Parser Content
```Java
{
Name = beyondtrust-bi-leef-app-notification-success-system
  Vendor = BeyondTrust
  Product = BeyondInsight
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """cat=System""", """CEF:""", """|BeyondTrust|BeyondInsight|""", """|PBPS|System|""", """Description=Internal process""" ]
  Fields = [
    """rt=({time}\w{3} \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """BeyondTrustBeyondInsightClientHost=({host}[\w.-]+)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """Operation=({operation}[^=]+)\s\w+=""",
    """ObjectType=({object_type}[^=]+?)\s\w+=""",
    """ObjectID=({object_id}[^=]+)\s\w+="""",
    """({app}BeyondInsight)"""
  ]


}
```
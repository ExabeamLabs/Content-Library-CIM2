#### Parser Content
```Java
{
Name = beyondtrust-powerbroker-kv-user-privilege-use-success-elevation
  Vendor = BeyondTrust
  Product = BeyondInsight
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [  """|BeyondTrust|""","""Application Requested Elevation""","""BeyondTrustBeyondInsightEventTypeID=28691""" ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}[\w\-.]+) CEF""",
    """\|rt=({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)""",
    """BeyondTrustBeyondInsightUserName =(?: |({user}[\w\.\-]{1,40}\$?)\s+\w+=)""",
    """BeyondTrustBeyondInsightPath=(?: |({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/"]+?))\s+\w+=)""",
    """BeyondTrustBeyondInsightAssetName =(?: |({src_host}.+?)\s+\w+=)""",
    """BeyondTrustBeyondInsightUserType=(?: |({privileges}.+?)\s*$)""",
    """deviceExternalId=({event_code}pbw|pbmac)""",
  ]
  ParserVersion = "v1.0.0"


}
```
#### Parser Content
```Java
{
Name = beyondtrust-prividentity-cef-app-activity-success-pbpsadmin
  ParserVersion = v1.0.0
  Conditions = [ """cat=System""", """CEF:""", """|BeyondTrust|BeyondInsight|""", """|PBPS|Administrators|""" ]

cef-beyondtrust-app-activity-events = {
  Vendor = BeyondTrust
  Product = BeyondTrust Privileged Identity
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields = [
    """rt=({time}\w{3} \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
	  """BeyondTrustBeyondInsightClientHost=({host}[\w.-]+)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sduser=(-|({email_address}[^@"\s]+@[^@"\s]+)|((({domain}[^\s]+?)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
    """\ssuser=(-|({email_address}[^@"\s]+@[^@"\s]+)|((({domain}[^\s]+?)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
    """Operation=({operation}[^=]+?)\s\w+=""",
    """ObjectType=({object_type}[^=]+?)\s\w+=""",
    """ObjectID=({object_id}[^=]+)\s\w+="""",
    """({app}BeyondInsight)"""
  
}
```
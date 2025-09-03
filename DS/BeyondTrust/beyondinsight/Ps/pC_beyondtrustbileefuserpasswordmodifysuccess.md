#### Parser Content
```Java
{
Name = beyondtrust-bi-leef-user-password-modify-success
  Conditions = [ """LEEF:""", """|BeyondTrust|BeyondInsight|""", """EventDesc=Password change is successful""", """cat=Change""" ]
  ParserVersion = "v1.0.0"

leef-beyondtrust-beyondinsight = {
   Vendor = BeyondTrust
   Product = BeyondInsight
   TimeFormat = "MMM dd yyyy HH:mm:ss"
   Fields = [
    """cat=({event_name}[^=]+?)(\\t|\\r|\\n|\\s)*\w+=""",
    """EventDesc=({event_name}[^=]+?)(\\t|\\r|\\s|\\)\w+=""",
    """devTime=({time}\w{3}\s+\d\d\s+\d\d\d\d\s+\d\d:\d\d:\d\d)""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """EventName =({category}[^=]+?)(\\t|\\r|\\n|\\s|=)""",
    """HostName =({host}[^=]+?)(\\t|\\r|\\n|\\s)*\w+=""",
    """UserName =({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\t|\\r|\\n|\\s)*\w+=""",
    """Message=({additional_info}[^=]+?)(\\t|\\r|\\n|\\s)*\w+=""",
    """Result=({result}[^=]+?)(\\t|\\r|\\n|\\s)*\w+="""
   ]
 }
 kv-beyondtrust-prividentity= {
  Vendor = BeyondTrust
  Product = BeyondTrust Privileged Identity
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","M/dd/yyyy HH:mm:ss a","M/d/yyyy HH:mm:ss a","MM/dd/yyyy HH:mm:ss a"] 
  Fields = [
    """\WLogTime:\s"({time}\d+\/\d+\/\d\d\d\d\s+\d+:\d+:\d+\s+(AM|PM|am|pm))","""
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)\s"""
    """\WCategory:\s"({category}[^"]+)","""
    """\WSource Host:\s"({src_host}[\w-.]+)""""
    """\WEvent Name:\s"({event_name}[^"]+)","""
    """\WSource IP:\s"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?","""
    """\WAgent ID:\s"({agent_id}[^"]+)","""
    """\WAgent Ver:\s"({version}[^"]+)","""
    """\WEvent Severity:\s"({result}[^"]+)","""
    """\WEvent Subject:\s"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","""
    """\WUser:\s"(({domain}[^\\]+)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)","""
    """\WUserID:\s"({user_id}[^"]+)","""
    """\WRoleUsed:\s"({role}[^"]+)","""
    """\WOperation:\s"({operation}[^"]+)","""
    """\WObjectType:\s"({object_type}[^"]+)","""
    """\WObjectID:\s"({object_id}[^"]+)","""
    """\WDetails:\s"({operation_details}[^"]+)","""
    """\WReason:\s"({result_reason}[^"]+)","""
    """\WLogID:\s"({event_id}[^"]+)","""
    """\WIPAddress:\s"({origin_ip}[^"]+)","""
    """\WManagedSystem=({account_domain}[^\s]+)\s"""
    """\sManagedAccount=({account_name}[^"]+)""""
    """\WAccountName:\s"({account_name}[^"]+)""""
    """\WResult:\s"({result}[^"]+)""""
    """\WManagedAccountID:\s"({account_id}[^"]+)""""
    """\WEvent Desc:\s"({description}[^"]+)""""
    """\WSecretType:\s"({object_type}[^"]+)","""
    """\WSecretId:\s"({object_id}[^"]+)","""
    """\WAuditID:\s"({audit_id}[^"]+)","""
    """\WDescription:\s"({additional_info}[^"]+)","""
  
}
```
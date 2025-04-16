#### Parser Content
```Java
{
Name = beyondtrust-rs-kv-meeting-modify-success-conferenceownerchanged
  Conditions = [ """|BeyondTrust|Remote Support Appliance|""", """|Conference Owner Changed|""", """|sessionId=""", """deviceHost=""" ]
  ParserVersion = "v1.0.0"

beyondtrust-remote-support-events = {
    Vendor = BeyondTrust
    Product = BeyondTrust Remote Support
    TimeFormat = "MMM dd HH:mm:ss"
    Fields = [
      """\|deviceHost=({host}[\w\-.]+)\|""",
      """\|hostname=({host}[\w\-.]+)\|""",
      """({time}\w{3}\s+\d+\s+\d\d:\d\d:\d\d)\|""",
      """\|BeyondTrust\|Remote Support Appliance\|[^\|]*\|({event_code}\d+)\|({event_name}[^\|]+)\|""",
      """\|sessionId=({session_id}[^\|]+)\|""",
      """\|dstUser=(({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)|({dest_user_full_name}[^\|]+))\|""",
      """\|dstHost=({dest_host}[\w\-.]+)\|""",
      """\|dstAddr=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\|""",
      """\|dstPort=({dest_port}\d+)\|""",
      """\|dstUid=((\d{1,3}\.){3}\d{1,3}|({dest_user_id}[^\|]+))\|""",
      """\|srcUser=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^\|]+))\|""",
      """\|srcHost=({src_host}[\w\-.]+)\|""",
      """\|srcAddr=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\|""",
      """\|srcPort=({src_port}\d+)\|""",
      """\|srcUid=({user_id}[^\|]+)\|""",
      """\|username=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^\|]+))\|""",
      """\|confMemOs=({os}[^\|]+)\|""",
      """\|msg=({additional_info}[^\|]+)\|"""
    ]
 }

 leef-beyondtrust-beyondinsight = {
   Vendor = BeyondTrust
   Product = BeyondInsight
   TimeFormat = "MMM dd yyyy HH:mm:ss"
   Fields = [
    """cat=({event_name}[^=]+?)(\\t|\\r|\\n|\\s)*\w+=""",
    """EventDesc=({event_name}[^=]+?)(\\t|\\r|\\s|\\)\w+=""",
    """devTime=({time}\w{3}\s+\d\d\s+\d\d\d\d\s+\d\d:\d\d:\d\d)""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """EventName =({category}[^=]+?)(\\t|\\r|\\n|\\s|=)""",
    """HostName =({host}[^=]+?)(\\t|\\r|\\n|\\s)*\w+=""",
    """UserName =({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\t|\\r|\\n|\\s)*\w+=""",
    """Message=({additional_info}[^=]+?)(\\t|\\r|\\n|\\s)*\w+=""",
    """Result=({result}[^=]+?)(\\t|\\r|\\n|\\s)*\w+="""
   ]
 
}
```
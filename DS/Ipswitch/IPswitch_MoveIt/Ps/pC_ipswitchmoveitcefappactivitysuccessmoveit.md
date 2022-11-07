#### Parser Content
```Java
{
Name = ipswitch-moveit-cef-app-activity-success-moveit
  Vendor = Ipswitch
  Product = IPswitch MoveIt
  TimeFormat = "epoch"
  ParserVersion = "v1.0.0"
  Conditions = [ """|IPswitch|MoveIt|""","""dvc=""" ]
  Fields = [
	"""\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
	"""\sdvchost=({host}[^\s]+)\s\w+=""",
    """\srt=({time}\d+)""",
    """\ssuser=({account_id}.+?)\s(\w+=|$)""",
    """\ssrc=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sshost=({dest_host}[^\s]+)\s\w+=""",
    """requestClientApplication=({browser}.+?)\s\w+=""",
    """fname=({file_name}.+?)\s\w+=""",
    """fname=[^.]+({file_ext}.+?)\s\w+=""",
    """filePath=({file_dir}.+?)\s\w+=""",
    """fileId=({file_id}\d+)\s\w+=""",
    """\s({file_type}file|File)""",
    """\|IPswitch\|MoveIt\|([^|]*\|){2}({operation}.+?)( at \d+\/\d+\/\d+ \d+:\d+:\d+|\|)""",
    """({app}MoveIt)"""
	"""\smsg=({additional_info}.+?)\sart=""",
  ]
   DupFields=["file_name->object_value",
     "account_id->user",
     "browser->user_agent",
     "operation->access"]


}
```
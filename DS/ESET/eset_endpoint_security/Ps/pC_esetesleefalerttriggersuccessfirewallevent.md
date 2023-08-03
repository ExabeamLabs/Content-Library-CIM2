#### Parser Content
```Java
{
Name = eset-es-leef-alert-trigger-success-firewallevent
  Conditions = [ """LEEF:""", """|ESET|RemoteAdministrator|""", """cat=ESET Firewall Event""" ]
  Fields = ${ESETParsersTemplates.eset-activity.Fields}[
    """eventDesc=({alert_name}[^=]+?)\s*(\w+=|$)""",
    """scannerID=({additional_info}[^=]+?)\s*(\w+=|$)""",
    """\Wsev=({alert_severity}\d+)"""
  ]
  DupFields = ["event_name->alert_type"]
  ParserVersion = "v1.0.0"

eset-activity = {
    Vendor = ESET
    Product = ESET Endpoint Security
    TimeFormat = "MMM dd yyyy HH:mm:ss z"
    Fields = [
      """\WdevTime=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d [^\s]+)""",
      """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """srcPort=({src_port}\d+)""",
      """dstPort=({dest_port}\d+)""",
      """\|ESET\|(?:[^\|]+\|){2}({event_name}[^\|]+)""",
      """actionTaken=({action}[^=]+?)\s*(\w+=|$)""",
      """\Wresult=({result}[^=]+?)\s*(\w+=|$)""",
      """\Wdetail=({additional_info}[^.]+)\.""",
      """objectUri=({url}[^\s]+?)\s*(\w+=|$)""",
      """deviceName =({host}[^\s]+)""",
      """hash=({hash_sha256}[^\s]+)""",
      """inbound=({direction}\d+)""",
      """\Waction=({operation}[^\s]+)\s""",
      """\Wcat=({category}[^=]+?)\s*(\w+=|$)""",
      """\Wuser=({user}[^\s=]+?)\s*(\w+=|$)""",
      """processName =({process_path}({process_dir}(?:(\w+:)*([\\\/]+[^=\\\/"]+)+)?[\\\/]+)({process_name}[^=\,\\\/]+?))\s*(\w+=|$)""",
      """proto=({protocol}[^\s]+)""",
      """\Wuser '(({domain}[^\s\\]+)\\)?({user}[\w\.\-]{1,40}\$?)'.""",
      """accountName =(NT AUTHORITY\\+|({domain}[^\\]+?)\\+)?(SYSTEM|({user}[^=\s]+?))\s*(\w+=|$)"""
    
}
```
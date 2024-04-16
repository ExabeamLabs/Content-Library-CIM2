#### Parser Content
```Java
{
Name = eset-es-leef-alert-trigger-success-threatevent
    Vendor = ESET
    Product = ESET Endpoint Security
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Conditions = [ """LEEF:""", """|ESET|RemoteAdministrator|""","""cat=ESET Threat Event""","""threatType=""" ]
    Fields = [
      """deviceName =({host}[^\s]+)\s""",
      """\Wcat=({threat_category}[^=]+?)\s*(\w+=|$)""",
      """\Wsev=({alert_severity}\d+)""",
      """\WdevTime=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
      """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """threatType=({alert_type}[^=]+?)\s*(\w+=|$)""",
      """\|ESET\|(?:[^\|]+\|){2}({alert_type}[^\|]+)""",
      """threatName =({alert_name}[^=]+?)\s*(\w+=|$)""",
      """eventDesc=({alert_name}[^=]+?)\s*(\w+=|$)""",
      """objectUri=({malware_url}[^=]+?)\s*(\w+=|$)""",
      """actionTaken=({action}[^=]+?)\s*(\w+=|$)""",
      """accountName =((({domain}[^\\=]+?)\\+)?({user}[\w\.\-]{1,40}\$?))\s*(\w+=|$)""",
      """engineVersion=({engine_version}\d+)""",
      """objectType=({object_type}[^=]+?)\s*(\w+=|$)""",
      """threatHandled=({threat_handled}\d+)""",
      """needRestart=({need_restart}\d+)""",
      """circumstances=({circumstances}[^=]+?)\s*(\w+=|$)""",
      """firstseen=({firstseen}[^=]+?)\s*(\w+=|$)""",
      """hash=({hash_sha256}[^\s]+)"""
    ]
    DupFields = ["action->additional_info", "host->dest_host", "malware_url->process_name"]
	ParserVersion = "v1.0.0"
  

}
```
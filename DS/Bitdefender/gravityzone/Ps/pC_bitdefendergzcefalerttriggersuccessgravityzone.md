#### Parser Content
```Java
{
Name = bitdefender-gz-cef-alert-trigger-success-gravityzone
  Vendor = Bitdefender
  Product = GravityZone
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF:""", """|Bitdefender|GravityZone"""]
  Fields = [
    """BitdefenderGZDetectionTime=({time}(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} 20\d{2} \d{1,2}:\d{1,2}:\d{1,2})""",
    """CEF:0\|Bitdefender\|GravityZone\|.*?\|\d+\|({operation}[^\|]+)\|"""
    """\d\d:\d\d:\d\d ({host}[\w\-.]+) \w+: CEF:""",
    """dvchost=({dest_host}.*?)\s\w+=""",
    """dvc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """BitdefenderGZAttackType=({alert_type}.*?)\s\w+=""",
    """BitdefenderGZMalwareName =({alert_name}.*?)\s\w+=""",
    """act=({action}.*?)\s\w+=""",
    """filePath=({file_path}.*?)\s\w+=""",
    """BitdefenderGZMalwareName.*?filePath=({malware_url}.*?)\s\w+=""",
    """BitdefenderGZMalwareType=({file_type}.*?)\s\w+=""",
    """BitdefenderGZDetectionLevel=({alert_severity}.*?)\s\w+=""",
    """suid=({suid}.*?)\s\w+=""",
    """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^"\s]+)""",
    """BitdefenderGZApplicationControlType=({protocol}[^\s]+)\s({method}[^=]+)=({url}.*?)\s\w+=""",
    """BitdefenderGZFwProtocolId=({protocol}.*?)\s\w+=""",
    """BitdefenderGZExploitType=({alert_type}.*?)\s\w+=""",
  ]
  DupFields = ["alert_severity->detection_level", "operation->bitdefender_activity_type"]


}
```
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
    """dvc=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """BitdefenderGZAttackType=({alert_type}.*?)\s\w+=""",
    """BitdefenderGZMalwareName =({alert_name}.*?)\s\w+=""",
    """act=({action}.*?)\s\w+=""",
    """filePath=({file_path}.*?)\s\w+=""",
    """BitdefenderGZMalwareName.*?filePath=({malware_url}.*?)\s\w+=""",
    """BitdefenderGZMalwareType=({file_type}.*?)\s\w+=""",
    """BitdefenderGZDetectionLevel=({alert_severity}.*?)\s\w+=""",
    """suid=({suid}.*?)\s\w+=""",
    """suser=({user}[^\s]+)""",
    """suser=({user}[^@]+)@({domain}[^"\s]+)""",
    """BitdefenderGZApplicationControlType=({protocol}[^\s]+)\s({method}[^=]+)=({url}.*?)\s\w+=""",
    """BitdefenderGZFwProtocolId=({protocol}.*?)\s\w+=""",
    """BitdefenderGZExploitType=({alert_type}.*?)\s\w+=""",
  ]
  DupFields = ["alert_severity->detection_level", "operation->bitdefender_activity_type￼"]


}
```
#### Parser Content
```Java
{
Name = pan-gp-cef-app-activity-success-gatewayhipcheck-1
  ParserVersion = "v1.0.0"
  Conditions = [ """|gateway-hip-check|GLOBALPROTECT|""", """GPSourceUser=""" ]
  Fields = ${PaloAltoParsersTemplates.paloalto-app-activity.Fields}[
    """({event_name}gateway-hip-check)"""
  ]
  DupFields = [ "event_name->operation" ]

paloalto-app-activity = {
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = "MMM dd yyyy HH:mm:ss zzz"
  Fields = [
    """GPClientHostName =(|({host}[\w.-]*?))\s+\w+?=""",
    """rt=({time}\w{3}\s\d{2}\s\d{4}\s(\d{2}:){2}\d{2}\s\S{3})\s""",
    """GPClientPrivateIPv4=({src_translated_ip}[A-Fa-f0-9.:]+)""",
    """ClientPublicIPv4=({src_ip}[A-Fa-f0-9.:]+)""",
    """GPSourceUser=(({domain}[^\\\s,]+)\\+)?({user}[^\\\s,]+)""",
    """dvchost=({src_host}[\w.-]+?)\s""",
    """GPClientOS=(|({os}[^=]*?))(\s+)?\w+?=""",
    """msg="({additional_info}[^"]+?)"""",
    """GPStatus=({result}\S+?)\s""",
    """({app}GLOBALPROTECT)"""
  
}
```
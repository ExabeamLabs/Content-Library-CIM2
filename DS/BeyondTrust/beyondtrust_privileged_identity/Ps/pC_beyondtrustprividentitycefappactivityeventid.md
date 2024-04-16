#### Parser Content
```Java
{
Name = beyondtrust-prividentity-cef-app-activity-eventid
  Conditions = [ """CEF:""", """|Privileged Identity|""", """|EVENT_ID_""" ]
  ParserVersion = "v1.0.0"

beyondtrust-pi-events {
  Vendor = BeyondTrust
  Product = BeyondTrust Privileged Identity
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields = [
    """\d\d:\d\d:\d\d ({host}[\w\-.]+) CEF""",
    """rt=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """msg=({additional_info}.+?)\s+(\w+=|$)""",
    """dntdom=\[?({domain}.+?)\]?\s+(\w+=|$)""",
    """duser=(\\)*((?i)(user|administrator)|({user}[\w\.\-]{1,40}\$?))\s+(\w+=|$)""",
    """cs3=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """CEF:\d+\|([^\|]+\|){3}({event_name}[^\|]+)\|""",
    """cs1=.+?({result}Success|Failure)"""
       
}
```
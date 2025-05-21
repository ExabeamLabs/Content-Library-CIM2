#### Parser Content
```Java
{
Name = manageengine-adssp-cef-user-password-reset-fail-notification
  Conditions= [ """CEF:0|ManageEngine|ADSSP|""", """dvchost""", """DATE_TIME""", """Notification""" ]
  ParserVersion = v1.0.0

adssp-system-info-events = {
  Vendor = ManageEngine
  Product = ADSSP
  TimeFormat = "epoch"
  Fields = [
    """DATE_TIME\\?=({time}\d{2}-\w{3}-\d\d \d{2}:\d{2} (?i:am|pm))""",
    """TIME\\?=({time}\d{13})""",
    """dvchost=({host}[\w\-.]+)""",
    """LOGIN NAME\\?=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """DOMAIN NAME\\?=(-|({domain}[^\]]+))""",
    """IP\\?=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """ACTION_NAME\\?=(-|({event_name}[^\]]+))""",
    """STATUS\\?=({additional_info}[^\]]+)"""
  
}
```
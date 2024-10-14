#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-user-privilege-use-success-esm
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ "|McAfee|ESM", "43-263046730"]
  Fields = [
    """({event_name}A privileged service was called.)""",
    """\|McAfee\|[^|]+?\|[^|]+?\|43-2630({event_code}\d+)(0|1)\|""",
    """\srt=({time}\d{13})\s+cnt""",
    """shost=({host}[\w\-.]+)""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """sntdom=({domain}[^\s]+)""",
    """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """nitroPrivileges=({privileges}.+?)(\s+\w+=|"*\s*$)""",
    """\sact=({result}[^\s]+)""",
    """nitroSource_Logon_ID=({login_id}.+?)(\s+\w+=|"*\s*$)""",
    """nitroSecurity_ID=({user_sid}.+?)(\s+\w+=|"*\s*$)""",
  ]
  DupFields = ["host->dest_host"]


}
```
#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-ds-object-modify-success-43
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch"
  Conditions = [ """|McAfee|ESM""", """43-263051360"""]
  Fields = [
    """({event_name}A directory service object was modified.)""",
    """\|McAfee\|[^|]+?\|[^|]+?\|43-2630({event_code}\d+)(0|1)\|""",
    """\srt=({time}\d{13})(\s+\w+=|"*\s*$)""",
    """shost=({host}[^\s]+)""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """sntdom=({domain}[^\s]+)""",
    """suser=({user}[\w\.\-]{1,40}\$?)""",
    """nitroUserIDSrc=({user}[\w\.\-]{1,40}\$?)(\s+\w+=|"*\s*$)""",
    """nitroSecurity_ID=({user_sid}.+?)(\s+\w+=|"*\s*$)""",
    """nitroSource_Logon_ID=({login_id}.+?)(\s+\w+=|"*\s*$)""",
    """nitroObjectID=({object_dn}.+?)(\s+\w+=|"*\s*$)""",
    """nitroObjectID=.*?({object_ou}(OU|ou).+?)(\s+\w+=|"*\s*$)""",
    """nitroTarget_Class=({object_class}.+?)(\s+\w+=|"*\s*$)"""
  ]
  ParserVersion = "v1.0.0"


}
```
#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-endpoint-notification-success-esm
    Vendor = Microsoft
    Product = Event Viewer - Security
  ParserVersion = v1.0.0
    TimeFormat = "epoch"
    Conditions = [ """|McAfee|ESM""", """43-26304611"""]
    Fields = [ """\|McAfee\|[^|]+?\|[^|]+?\|43-2630({event_code}\d+)(0|1)\|""",
      """\srt=({time}\d{13})\s+cnt""",
      """shost=({host}[^\s]+)""",
      """nitroAppID=({process_name}.+?)\s+\w+=""",
      """sntdom=({domain}[^\s]+)""",
      """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+""",
      """nitroSecurity_ID=({user_sid}[^\s]+)""",
      """nitroSource_Logon_ID=({login_id}[^\s]+)"""
    ]
    DupFields=[ "host->dest_host" ]
  

}
```
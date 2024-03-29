#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-privilege-use-success-4672-1
    Vendor = Microsoft
    Product = Event Viewer - Security
    ParserVersion = "v1.0.0"
    TimeFormat = "epoch"
    Conditions = ["CEF:", "|McAfee|ESM", "43-26304672"]
    Fields = [
      """({event_name}Special privileges assigned to new logon)""",
      """\|McAfee\|[^|]+?\|[^|]+?\|43-2630({event_code}\d+)(0|1)\|""",
      """\srt=({time}\d{13}?)(\s|0\||$)""",
      """\ssrc=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(:({dest_port}\d+))?(\s|0\||$)""",
      """\sshost=({dest_host}[^\s]+?)(\s|0\||$)""",
      """\ssntdom=({domain}[^\s]+?)(\s|0\||$)""",
      """\ssuser=({user}.+?)(\s+\w+=|0\|\s*$)""",
      """\sact=({result}.+?)(\s+\w+=|0\|\s*$)""",
      """\snitroSource_Logon_ID=({login_id}.+?)(\s|0\||$)""",
      """\snitroPrivileges=({privileges}.+?)(\s+\w+=|0\|\s*$)""",
    ]
    DupFields = ["dest_ip->host", "dest_host->host"]
  

}
```
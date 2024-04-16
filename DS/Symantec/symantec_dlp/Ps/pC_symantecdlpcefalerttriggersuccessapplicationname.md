#### Parser Content
```Java
{
Name = symantec-dlp-cef-alert-trigger-success-applicationname
    Vendor = Symantec
    Product = Symantec DLP
    Conditions = [ """CEF:""", """Symantec|DLP""","""POLICY=""", """MONITOR_NAME=""", """APPLICATION_NAME=""" ]
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """({host}\S+)\s+CEF:""",
      """\WINCIDENT_ID=({alert_id}\d+)""",
      """\WPOLICY=({alert_name}[^=]+)\s\w+=""",
      """\WSEVERITY=\d+:({alert_severity}[^=]+)\s\w+=""",
      """\WPROTOCOL=({protocol}[^=]+)\s\w+=""",
      """\WBLOCKED=(None|({action}[^=]+))\s\w+=""",
      """\WSENDER=({src_ip}[A-Fa-f.:\d]+)\s+\w+=""",
      """\WENDPOINT_MACHINE=(N\/A|({src_host}[^=]+))\s\w+="""
      """\WRECIPIENTS=(N\/A|({target}[^=]+))\s\w+=""",
      """\WRECIPIENTS=(N\/A|({recipients}[^@]+@[^=]+))\s\w+=""",
      """\WSUBJECT=+\s*(N\/A|({email_subject}[^=]+))\s\w+=""",
      """\WATTACHMENT_FILENAME=\s*(N\/A|({file_dir}[^=]+[\\\/])?({file_name}[^\s]+(\.({file_ext}[^\s]+))?))\s*\w+=""",
      """\WSENDER=((WinNT:\/+({domain}[^\/]+)\/({user}[\w\.\-]{1,40}\$?))|({email_address}[^@]+@[^=]+))\s\w+=""",
    ]
    DupFields = [ "email_subject->additional_info" , "email_address->src_email_address"]
    SOAR {
      IncidentType = "dlp"
      DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "user->dlpUser", "alert_name->dlpPolicy", "alert_severity->sourceSeverity", "protocol->dlpProtocol", "action->dlpActionTaken"]
      NameTemplate = """Symantec DLP Alert ${alert_name} found"""
      ProjectName = "SOC"
      EntityFields = [
        {EntityType="user", Name ="windows_id", Fields=["user->windows_id"]

}
```
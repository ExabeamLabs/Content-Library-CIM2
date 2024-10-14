#### Parser Content
```Java
{
Name = claroty-ctd-cef-alert-trigger-success-newconflictasset
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """|Schneider|CTD|""", """|New Conflict Asset|""", """|CtdSourceIp=""" ]
  DupFields = ["event_name->alert_name", "alert_name->alert_type", "severity->alert_severity"]


}
```
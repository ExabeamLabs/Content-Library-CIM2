#### Parser Content
```Java
{
Name = claroty-ctd-cef-alert-trigger-success-newasset
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """|CTD|""", """|New Asset|""", """|CtdSourceIp=""" ]
  DupFields = ["event_name->alert_name", "alert_name->alert_type", "severity->alert_severity"]


}
```
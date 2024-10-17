#### Parser Content
```Java
{
Name = mcafee-dlp-kv-alert-trigger-success-plug
    Vendor = McAfee
    Product = McAfee DLP Endpoint
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """Block""", """DEVICE_""" , """EventType_LocalizationKey""", """PLUG"""]
    Fields = [
        """LocalTime="({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)"""
        """UTCTime(=|:)\s*"({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)""",
        """ComputerName(=|:)\s*"({src_host}[^"]+)"""",
        """UserName(=|:)\s*"(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
        """ReactionSet_DisplayName(=|:)\s*"([^"\?]+\?)?({alert_type}\w+)""",
        """Policy_Name(=|:)\s*"({alert_name}[^"]+)"""",
        """Evidence(=|:)\s*"([^,]*,){4}\s*({device_id}.+?)(\"|&\d|,)""",
        """Evidence(=|:)\s*"([^,]*,)\s*({device_type}[^,]+)""",
        """EventTypeDisplayName(=|:)\s*"({additional_info}[^"]+)""""
    ]
    SOAR {
      IncidentType = "dlp"
      DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "user->dlpUser", "alert_name->dlpPolicy", "alert_type->dlpActionTaken", "src_host->dlpDeviceName"]
      NameTemplate = """McAfee DLP Alert ${alert_name} found"""
      ProjectName = "SOC"
      EntityFields = [
        {EntityType="device", Name ="src_address", Fields=["src_host->host_name"]

}
```
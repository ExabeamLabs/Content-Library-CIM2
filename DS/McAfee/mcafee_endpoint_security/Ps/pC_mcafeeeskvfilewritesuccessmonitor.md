#### Parser Content
```Java
{
Name = mcafee-es-kv-file-write-success-monitor
    Vendor = McAfee
    Product = McAfee Endpoint Security
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """ApplicationSet_DisplayName""", """OUTGOING_FS_REMOVABLE""", "Monitor" ]
    Fields = [
        """UTCTime:\s*"({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)""",
        """ComputerName(=|:)\s*"({dest_host}[^"]+)"""",
        """(\s|,)Evidence(=|:)\s*"({file_path}[^,]+)""",
        """(\s|,)Evidence(=|:)\s*"[^",]+\\({file_name}[^,\\]+?(\.({file_ext}[^\s\.\\,]+?))?),""",
        """ProcessInfo_FileName(=|:)\s*"({process_name}[^"]+)""",
        """EventType_LocalizationKey(=|:)\s*"({operation}[^"]+)"""",
        """TotalContentSize(=|:)\s*"({bytes}\d+)"""",
        """UserName(=|:)\s*"(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
        """ReactionSet_DisplayName(=|:)\s*"({action}[^"]+)"""",
        """EventTypeDisplayName(=|:)\s*"({operation_details}[^"]+)"""",
    ]
	ParserVersion = "v1.0.0"
  

}
```
#### Parser Content
```Java
{
Name = mcafee-es-kv-file-write-success-localizationkey
    Vendor = Trellix
    Product = Trellix Endpoint Security
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """DEVICE_PLUG""" , """EventType_LocalizationKey"""]
    Fields = [
        """({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s*UTC""",
        """UTCTime:\s*"({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)""",
        """ComputerName(=|:)\s*"({dest_host}[^"]+)"""",
        """Evidence(=|:)\s*"([^,]*,){4}\s*({device_id}.+?)(\"|&\d|,)""",
        """Evidence(=|:)\s*"([^,]*,)\s*({device_type}[^,]+)""",
        """EventType_LocalizationKey(=|:)\s*"({operation}[^"]+)"""",
        """UserName(=|:)\s*"(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
        """FocusDisplay(=|:)\s*"({operation_details}[^"]+)"""",
    ]
	ParserVersion = "v1.0.0"
  

}
```
#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-file-time-modify-2-1-tl"
    ParserVersion = "v1.0.0"
    Conditions = [
      "<eventid>2</eventid>"
      "<provider name='microsoft-windows-sysmon'"
    ]
    DupFields = [
      "host->dest_host"
    ]
  

}
```
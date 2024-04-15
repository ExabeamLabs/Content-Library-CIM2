#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-registry-12-tl"
    ParserVersion = "v1.0.0"
    Conditions = [
      "<eventid>12</eventid>"
      "<provider name='microsoft-windows-sysmon'"
    ]
    DupFields = [
      "host->dest_host"
    ]
  

}
```
#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-dll-load-7-tl"
    ParserVersion = "v1.0.0"
    Conditions = [
      "<eventid>7</eventid>"
      "<provider name='microsoft-windows-sysmon'"
    ]
    DupFields = [
      "process_name->src_process_name"
    ]
  

}
```
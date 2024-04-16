#### Parser Content
```Java
{
Name = "microsoft-defenderep-json-file-success-advancedhuntingdevicefileevents"
  ExtractionType = json
  Conditions = [ """DeviceFileEvents"""", """"ActionType":""", """"FileName":""" ]
  DupFields = ["action->operation"]
  ParserVersion = "v1.0.0"


}
```
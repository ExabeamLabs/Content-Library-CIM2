#### Parser Content
```Java
{
Name = "microsoft-o365-cef-app-file-memberremoved"
Conditions = [
  """CEF:"""
  """|Microsoft Teams|"""
  """|MemberRemoved|"""
]
ParserVersion = "v1.0.0"

xml-ms-event-viewer.Fields}[
    """<Computer>({host}[\w\-.]+)"""
  
}
```
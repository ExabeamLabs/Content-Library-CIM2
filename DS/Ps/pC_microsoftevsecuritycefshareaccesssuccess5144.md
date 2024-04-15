#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-share-access-success-5144"
Conditions = [
  """|Microsoft|Microsoft Windows|"""
  """A network share object was deleted"""
  """Microsoft-Windows-Security-Auditing:5144|"""
]
ParserVersion = "v1.0.0"

windows-events-3.Fields} [
      """({event_name}A network share object was modified)""",
      """({event_code}5143)""",
      
}
```
#### Parser Content
```Java
{
Name = "microsoft-o365-cef-app-file-teams"
Conditions = [
  """CEF:"""
  """|Microsoft Teams|"""
  """|TeamsSessionStarted|"""
]
ParserVersion = "v1.0.0"

q-adfs-auth.Fields}[
    """\sComputer=({host}.+?)(\s+\w+=|\s*$)"""
  
}
```
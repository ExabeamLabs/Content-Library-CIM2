#### Parser Content
```Java
{
Name = "microsoft-o365-cef-app-file-tabadded"
Conditions = [
  """CEF:"""
  """|Microsoft Teams|"""
  """|TabAdded|"""
]
ParserVersion = "v1.0.0"

q-adfs-auth.Fields}[
    """\sComputer=({host}.+?)(\s+\w+=|\s*$)"""
  
}
```
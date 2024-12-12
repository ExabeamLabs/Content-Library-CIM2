#### Parser Content
```Java
{
Name = "microsoft-o365-cef-file-read-success-fileaccessed"
Conditions = [
  """|Microsoft|"""
  """|FileAccessed|"""
  """eventId="""
]
ParserVersion = "v1.0.0"

q-adfs-auth.Fields}[
    """\sComputer=({host}.+?)(\s+\w+=|\s*$)"""
  
}
```
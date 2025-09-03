#### Parser Content
```Java
{
Name = "microsoft-o365-cef-file-delete-success-filedeleted"
Conditions = [
  """|Microsoft|"""
  """|FileDeleted|"""
  """eventId="""
]
ParserVersion = "v1.0.0"

q-adfs-auth.Fields}[
    """\sComputer=({host}.+?)(\s+\w+=|\s*$)"""
  
}
```
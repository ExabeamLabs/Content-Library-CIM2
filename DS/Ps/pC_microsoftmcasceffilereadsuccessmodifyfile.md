#### Parser Content
```Java
{
Name = "microsoft-mcas-cef-file-read-success-modifyfile"
Conditions = [
  """CEF:"""
  """|MCAS|SIEM_Agent|"""
  """|Modify file|"""
]
ParserVersion = "v1.0.0"

q-adfs-auth.Fields}[
    """\sComputer=({host}.+?)(\s+\w+=|\s*$)"""
  
}
```
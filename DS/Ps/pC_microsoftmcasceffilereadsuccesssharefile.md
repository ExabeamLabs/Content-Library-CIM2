#### Parser Content
```Java
{
Name = "microsoft-mcas-cef-file-read-success-sharefile"
Conditions = [
  """CEF:"""
  """|MCAS|SIEM_Agent|"""
  """|Share file|"""
]
ParserVersion = "v1.0.0"

q-adfs-auth.Fields}[
    """\sComputer=({host}.+?)(\s+\w+=|\s*$)"""
  
}
```
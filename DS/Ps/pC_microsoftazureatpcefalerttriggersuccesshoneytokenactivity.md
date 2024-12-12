#### Parser Content
```Java
{
Name = microsoft-azureatp-cef-alert-trigger-success-honeytokenactivity
Conditions = [
  """CEF"""
  """|Microsoft|Azure ATP|"""
  """|HoneytokenActivitySecurityAlert|"""
]
ParserVersion = "v1.0.0"

q-adfs-auth.Fields}[
    """\sComputer=({host}.+?)(\s+\w+=|\s*$)"""
  
}
```
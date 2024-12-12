#### Parser Content
```Java
{
Name = microsoft-azuresc-json-alert-trigger-success-asc
Product = Microsoft Defender for Cloud
Conditions = [
  """"category":"""
  """"VM_LoginBruteForceValidUserFailed""""
  """"title":"""
  """"vendor":"""
  """"Microsoft""""
  """"provider":"""
  """"ASC""""
]
ExtractionType = json
ParserVersion = "v1.0.0"

q-adfs-auth.Fields}[
    """\sComputer=({host}.+?)(\s+\w+=|\s*$)"""
  
}
```
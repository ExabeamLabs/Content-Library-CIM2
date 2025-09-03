#### Parser Content
```Java
{
Name = "microsoft-azure-cef-file-read-success-actiontype"
Conditions = [
  """|beatname=eventhubbeat|"""
  """|device_type=eventhubbeat|"""
  """|subject=AdvancedHunting-DeviceEvents|"""
  """vmid="""
  """@timestamp"""
  """@metadata"""
  """"ActionType":"ReadProcessMemoryApiCall""""
]
ParserVersion = "v1.0.0"

q-adfs-auth.Fields}[
    """\sComputer=({host}.+?)(\s+\w+=|\s*$)"""
  
}
```
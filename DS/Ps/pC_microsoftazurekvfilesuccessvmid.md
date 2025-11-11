#### Parser Content
```Java
{
Name = "microsoft-azure-kv-file-success-vmid"
Conditions = [
  """|beatname=eventhubbeat|"""
  """|device_type=eventhubbeat|"""
  """|subject=AdvancedHunting-DeviceFileEvents|"""
  """vmid="""
  """@timestamp"""
  """@metadata"""
  """"ActionType":"""
]
ParserVersion = "v1.0.0"

q-adfs-auth.Fields}[
    """\sComputer=({host}.+?)(\s+\w+=|\s*$)"""
  
}
```
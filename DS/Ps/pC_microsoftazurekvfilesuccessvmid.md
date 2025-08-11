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
DupFields = ["event_category->category"]
ParserVersion = "v1.0.0"


}
```
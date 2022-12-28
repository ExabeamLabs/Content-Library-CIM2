#### Parser Content
```Java
{
Name = riverbedsteelhead-rs-str-app-notification-smbsign
    ParserVersion = "v1.0.0"
    Product = Riverbed Steelhead
    Vendor = Riverbed Steelhead
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """sport[""", """[smbsign""", """ Shutting down""" ]
    Fields = [
    """\s+({host}[\w\.-]+)\s+sport\[""",
    """\s+\{({src_ip}[\w\.-]+):({src_port}\d+)\s+({dest_ip}[\w\.-]+):({dest_port}\d+)\}""",
    """:\s+\[([^.]+).({priority}[^\]]+)\]""",#dl field removed
    """}\s+({event_name}.+?)(,|\.)""",
    """Reason\s+-\s+({reason}.+?)(\.|$)""",
    ]
  

}
```
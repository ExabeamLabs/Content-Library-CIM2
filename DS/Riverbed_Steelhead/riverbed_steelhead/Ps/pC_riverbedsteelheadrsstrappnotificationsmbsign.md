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
    """\s+\{({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)\s+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({dest_port}\d+)\}""",
    """:\s+\[([^.]+).({priority}[^\]]+)\]""",#dl field removed
    """}\s+({event_name}.+?)(,|\.)""",
    """Reason\s+-\s+({result_reason}.+?)(\.|$)""",
    ]
  

}
```
#### Parser Content
```Java
{
Name = riverbedsteelhead-rs-kv-network-notification-sport
    Product = Riverbed Steelhead
    Vendor = Riverbed Steelhead
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """sport[""", """[rpch""", """body content on""" ]
    Fields = [
    """\s+({host}[\w\.-]+)\s+sport\[""",
    """\s+\{({src_ip}[\w\.-]+):({src_port}\d+)\s+({dest_ip}[\w\.-]+):({dest_port}\d+)\}""",
    """:\s+\[([^.]+)\.({priority}[^\]]+)\]""", #dl field removed
    """\Whttp_bytes_received_=({bytes_in}\d+)""",
    """\Whttp_bytes_sent_=({bytes_out}\d+)""",
    """\Wcontent_length_=({bytes}\d+)""",
# chain_length is removed
    """}\s+({event_name}.+?)(,|\.)""",
    ]
  ParserVersion = "v1.0.0"
  

}
```
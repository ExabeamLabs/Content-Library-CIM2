#### Parser Content
```Java
{
Name = cisco-mma-kv-http-session-fail-url
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Meraki MX appliance
  TimeFormat = "epoch_sec"
  Conditions = [ """ events content_filtering_block """, """ url=""" ]
  Fields = [
    """({host}[\w.\-]+) ({time}\d+)\.\d+\s+\S+\s+events content_filtering_block""",
    """\scategory0='({category}[^']+)""",
    """\sserver='({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}):({dest_port}\d+)""",
    """\surl='({url}(({protocol}\w+):\/+)?({web_domain}[^\/']+)({uri_path}[^\?']+?)?({uri_query}\?.+?)?)'""",
  ]


}
```
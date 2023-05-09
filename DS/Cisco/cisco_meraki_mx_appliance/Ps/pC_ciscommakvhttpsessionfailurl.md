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
    """({host}[\w.\-]+) ({time}\d{10})\.\d+\s+\S+\s+events content_filtering_block""",
    """\scategory0='({category}[^']+)""",
    """\sserver='({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({dest_port}\d+)""",
    """\surl='({url}(({protocol}\w+):\/+)?({web_domain}[^\/']+)({uri_path}[^\?']+?)?({uri_query}\?.+?)?)'""",
  ]


}
```
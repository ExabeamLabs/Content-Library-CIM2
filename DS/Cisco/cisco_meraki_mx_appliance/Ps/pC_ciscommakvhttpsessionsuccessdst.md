#### Parser Content
```Java
{
Name = cisco-mma-kv-http-session-success-dst
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Meraki MX appliance
    TimeFormat = "epoch_sec"
    Conditions = [ """ urls """, """ request:""", """ src""", """ dst""" ]
    Fields = [
      """({time}\d{10})\.\d+\s+({host}[\w.\-]+)\s+urls\s""",
      """\scs6=\d+\-\d+\-\d+T\d\d:\d\d:\d\d\.\d+Z\s+({host}[a-fA-F\d.:]+)""",
      """\ssrc\\*=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)""",
      """\sdst\\*=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({dest_port}\d+)""",
      """\smac\\*=({src_mac}[a-fA-F\d:]+)""",
      """\sagent\\*='?({user_agent}.+?)'?\s*request:""",
      """\srequest:\s*(?:UNKNOWN|({method}\w+))\s+({url}(\w+:\/+)?({web_domain}[^\s:\/]+)(?:\:({dest_port}\d+))?({uri_path}\/[^\?]*?)?({uri_query}\?.+?)?)(\.\.\.)?\s*($|"|cs6=)""",
   ]
  

}
```
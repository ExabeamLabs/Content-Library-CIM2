#### Parser Content
```Java
{
Name = sophos-invincea-kv-alert-trigger-success-invincea
  Vendor = Sophos
  Product = Sophos Invincea
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """INVINCEA:""", """vendor=Invincea""", """product=Invincea""" ]
  Fields = [
        """\w{3}\s+\d{1,2}\s+\d{2}:\d{2}:\d{2}\s+({host}[^\s]+)""",
        """\s+name="({alert_name}[^\"]+)""",
        """severity=({alert_severity}\d+)\s+""",
        """src_host=({src_host}[^\s]+)""",
        """src_ip=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
        """product=({alert_type}[^\s]+)""",
        """request=({url}.+?)\s+num_exec""",
        """src_user=({user}.+?)\s+src_host"""
  ]
  DupFields = ["host->dest_host", "url->process_name"]
  ParserVersion = "v1.0.0"


}
```
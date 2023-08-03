#### Parser Content
```Java
{
Name = sophos-invincea-kv-alert-trigger-success-invincea
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """INVINCEA:""", """vendor=Invincea""", """product=Invincea""" ]
  Fields = [
        """\w{3}\s+\d{1,2}\s+\d{2}:\d{2}:\d{2}\s+({host}[^\s]+)""",
        """\s+name="({alert_name}[^\"]+)""",
        """severity=({alert_severity}\d+)\s+""",
        """src_host=({src_host}[^\s]+)""",
        """src_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
        """product=({alert_type}[^\s]+)""",
        """request=({malware_url}.+?)\s+num_exec""",
        """src_user=({user}[\w\.\-]{1,40}\$?)\s+src_host"""
  ]
  DupFields = ["host->dest_host", "malware_url->process_name"]
  ParserVersion = "v1.0.0"


}
```
#### Parser Content
```Java
{
Name = trendmicro-tippingpoint-str-alert-trigger-success-smb
  ParserVersion = v1.0.0
  Product = TippingPoint NGIPS
  TimeFormat = "epoch"
  Conditions = [ """00000001-0001-0001-0001-""", """ smb """ ]
  Fields = ${TippingPointParserTemplates.tippingpoint-sms-alert-template.Fields} [
    """00000001-0001-0001-0001-00000\d+\s+.+?\s+\d+\s+({protocol}smb)""",
    """00000001-0001-0001-0001-00000\d+\s+.+?\s+\d+\s+smb(\s+[^\s]+){4}\s+({hit_cnt}\d+)\s+""",
    """00000001-0001-0001-0001-00000\d+\s+.+?\s+\d+\s+smb(\s+[^\s]+){5}\s+({src_zone_name}[^\s]+)\s+({dest_zone}[^\s]+)""",
    """00000001-0001-0001-0001-00000\d+\s+.+?\s*\d+\s+smb(\s+[^\s]+){8}\s+({vlan_id}\d+)""",
    """00000001-0001-0001-0001-00000\d+\s+.+?\s*\d+\s+smb(\s+[^\s]+){9}\s+({host}[^\s]+)""",
    """00000001-0001-0001-0001-00000\d+\s+.+?\s*\d+\s+smb(\s+[^\s]+){11}\s+({time}\d{13})""",
    """00000001-0001-0001-0001-00000\d+\s+.+?\s*\d+\s+smb(\s+[^\s]+){12}\s+({alert_id}\d+)""",
    """smb\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+({src_port}\d+)\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+({dest_port}\d+)"""
  ]

tippingpoint-sms-alert-template = {
    Vendor = Trend Micro
    Product = TippingPoint NGIPS
    TimeFormat = "epoch"
    Fields = [
          """({alert_severity}\d)\s+([\w\d-])+\s00000001-0001-0001-0001-0000""",
          """\s+({event_code}[^\s]+)\s+00000001-0001-0001-0001-00000""",
          """00000001-0001-0001-0001-00000\d+\s+({alert_name}.+?)\s+\d+\s+""",
          """00000001-0001-0001-0001-00000\d+\s+.+?\s+\d+\s+[^\s]+\s+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s+({src_port}\d+)""",
          """00000001-0001-0001-0001-00000\d+\s+.+?\s+\d+\s+([^\s]+\s+){3}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s+({dest_port}\d+)""",
    ]
    SOAR {
      IncidentType = "generic"
      DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->description", "alert_severity->sourceSeverity"]
      NameTemplate = """TippingPoint Alert ${alert_name} found"""
      ProjectName = "SOC"
      EntityFields = [
        {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address"]},
        {EntityType="device", Name ="dest_address", Fields=["dest_ip->ip_address"]},
      ]
    }
  
}
```
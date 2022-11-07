#### Parser Content
```Java
{
Name = fireeye-endpointsecurity-cef-alert-trigger-success-iochitfound
  ParserVersion = "v1.0.0"
  Conditions = [ """|fireeye|HX|""", """ categoryTupleDescription=""", """|IOC Hit Found|""" ]

s-fireeye-hx-alert = {
    Vendor = FireEye
    Product = FireEye Endpoint Security (HX)
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Fields = [
      """\Wrt=({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)""",
      """\|fireeye\|([^\|]*\|){2}({alert_type}.+?)\|""",
      """\|fireeye\|([^\|]*\|){3}({alert_name}.+?)\|""",
      """\|fireeye\|([^\|]*\|){4}({alert_severity}.+?)\|""",
      """cs4=({alert_name}.+?)\s+(\w+=.+?\s+)$""",
      """\WexternalId=({alert_id}\d+)""",
      """\Wdntdom=(?:NA|({domain}.+?))(\s+\w+=|\s*$)""",
      """\Wdst=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\Wsuser=({user}[^\s]+)""",
      """\Wsuser=({email_address}[^\s@]+@[^\s]+)""",
      """\Wdhost=({src_host}[^\s]+)""",
      """\Wdvchost=({host}[^\s]+)""",
      """\Wmsg=({additional_info}.+?)\s+\w+="""
    ]
    SOAR {
      IncidentType = "malware"
      DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->malwareName", "alert_type->malwareCategory", "alert_severity->sourceSeverity", "src_host->malwareVictimHost"]
      NameTemplate = """FireEye Alert ${alert_name} found"""
      ProjectName = "SOC"
      EntityFields = [
        {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]}
      ]
    }
  
}
```
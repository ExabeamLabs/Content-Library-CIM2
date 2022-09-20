#### Parser Content
```Java
{
Name = pan-ngfw-json-alert-trigger-success-resetserver
  Vendor = Palo Alto Networks
  Product = NGFW
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"LogType":"THREAT"""", """"Subtype":"virus"""", """"Action":"reset-server"""" ]
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)""",
    """"host":"({host}[^"]+)"""",
    """"DeviceName":"({host}[^"\s]+)"""",
    """"PrivateIPv(4|6)":"({src_ip}[a-fA-F\d:.]+)""",
    """"PublicIPv(4|6)":"({dest_ip}[a-fA-F\d.:]+)""",
    """"Source(Address|IP)":"({src_ip}[a-fA-F\d:.]+)""",
    """"DestinationAddress":"({dest_ip}[a-fA-F\d:.]+)""",
    """"(Source)?User(Name)?":"((na|NA|({domain}[^"\\]+))\\+)?(({email_address}[^@"]+@[^\."]+\.[^"]+)|({user}[^"]+))"""",
    """"SourcePort":({src_port}\d+)""",
    """"DestinationPort":({dest_port}\d+)""",
    """"Protocol":"({protocol}[^"]+)"""",
    """"LogType":"({event_category}[^"]+)"""",
    """"Action":"({action}[^"]+)"""",
    """"VendorSeverity":"({alert_severity}[^"]+)"""",
    """"ThreatCategory":"({threat_category}[^"]+)"""",
    """"Subtype":"({alert_type}[^"]+)"""",
    """"ThreatID":"({alert_name}[^"\(]+)(\(({alert_id}\d+)\))?""",
    """"FileName":"({additional_info}[^"]+)""""
    """"FileName":"({file_name}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```
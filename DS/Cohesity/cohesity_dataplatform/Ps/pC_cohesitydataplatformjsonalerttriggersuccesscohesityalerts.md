#### Parser Content
```Java
{
Name = "cohesity-dataplatform-json-alert-trigger-success-cohesityalerts"
  Vendor = "Cohesity"
  Product = "Cohesity DataPlatform"
  TimeFormat = "MM/dd/yyyy HH:mm:ss"
  Conditions = [ """cohesity_alerts:""", """"AlertName"""", """"AlertSeverity"""" ]
  Fields = [
    """Timestamp:\s*({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d)\s"""
    """"ClusterName":\s*"({host}[^"]+)""""
    """"AlertSeverity":\s*"({alert_severity}[^"]+)""""
    """"AlertDescription":\s*"({additional_info}[^"]+)""""
    """"AlertName":\s*"({alert_name}[^"]+)""""
    """"AlertCode":\s*"({alert_id}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```
#### Parser Content
```Java
{
Name = google-gcpca-sk4-app-activity-stackdriverevents
  ParserVersion = v1.0.0
  Vendor = Google
  Product = GCP CloudAudit
  TimeFormat = "epoch"
  Conditions = [ """payload\=JsonPayload""", """destinationServiceName =Google Cloud Platform (GCP)""" ]
  Fields = [
    """timestamp\\=({time}\d{13})""",
    """, resource\\=.*?, labels\\=.*?cluster_name\\=({cluster_name}[^,\}]+)""",
    """, resource\\=.*?, labels\\=.*?instance_id\\=({instance_id}[^,\}]+)""",
# container_name is removed
# namespace_id is removed
    """, resource\\=.*?, labels\\=.*?project_id\\=({project_id}[^,\}]+)""",
    """, resource\\=.*?, labels\\=.*?zone\\=({zone}[^,\}]+)""",
# pod_id is removed
    """, resource\\=.*?, labels\\=.*?severity\\=({severity}[^,\}]+)""",
    """logName\\=({log_name}[^,\}]+)""",
# json_payload is removed
  ]


}
```
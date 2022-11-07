#### Parser Content
```Java
{
Name = exabeam-aa-kv-alert-trigger-success-anomaly
  ParserVersion = v1.0.0
  Vendor = Exabeam
  Product = Advanced Analytics
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """exabeam-analytics-master""","""base_risk_score="""","""alert_source="anomaly"""","""trigger_type="""" ]
  Fields = [
    """\salert_source="({alert_source}anomaly)""""
    """\sid="({container_id}[^"]+)"""",
    """\sscore="({original_risk_score}\d+)"""",
    """\suser="(\*+|({user}[^"]+))"""",
    """\sevent_type="({event_category}[^"]+)"""",
    """\srule_id="({rule_id}[^"]+)"""",
    """\srule_name="({rule}[^"]+)"""",
    """\srule_description="({rule_description}[^"]+)"""",
    """\srule_reason="({rule_reason}[^"]+)"""",
    """\strigger_type="({trigger_type}[^"]+)"""",
    """\strigger_entity="({trigger_entity}[^"]+)"""",
    """\surl="({url}[^"]+)"""",
    """\sevent_time="({event_time}\d+)"""",
    """\slog_time="({log_time}\d+)"""",
    """\sbase_risk_score="({base_risk_score}[\d.]+)"""",
    """\smitre_labels="({mitre_labels}[^"]+)"""",
    """\susecases="({rule_usecases}[^"]+)"""",
    """\sdomain="({domain}[^"]+)"""",
    """\shost="({host}[^"]+)"""",
    """\sdest_ip="({dest_ip}[^"]+)"""",
    """\sdest_host="({dest_host}[^"]+)"""",
    """\ssrc_ip="({src_ip}[^"]+)"""",
    """\ssrc_host="({src_host}[^"]+)"""",
    """\slabels="({asset_labels}[^"]+)"""",
    """\sincident_creation_time="({incident_creation_time}[^"]+)"""",
    """\ssource_event_id="({event_id}[^"]+)"""",
    """\ssession_id="({session_id}[^"]+)""""
  ]
  


}
```
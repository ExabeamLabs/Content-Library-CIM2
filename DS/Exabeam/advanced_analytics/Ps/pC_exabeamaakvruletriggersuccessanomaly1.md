#### Parser Content
```Java
{
Name = exabeam-aa-kv-rule-trigger-success-anomaly-1
    ParserVersion = v1.0.0
    Vendor = Exabeam
    Product = Advanced Analytics
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    log_timeFormat = "epoch"
    event_timeFormat = "epoch"
    incident_creation_timeFormat = "epoch"
    Conditions = ["""exabeam-analytics-master""", """base_risk_score="""", """alert_source="anomaly"""", """trigger_type="""", """rule="""]
    Fields = [
      """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)\s"""
      """\salert_source="({alert_source}anomaly)""""
      """\sid="({container_id}[^"]+)"""",
      """\sscore="({original_risk_score}\d+)"""",
      """\suser="(\*+|({user}[\w\.\-]{1,40}\$?))(\s*|")""",
      """\sevent_type="({event_category}[^"]+)"""",
      """rule="({rule}[^"]+)"""",
      """\srule_id="({rule_id}[^"]+)"""",
      """\srule_name="({rule}[^"]+)"""",
      """\srule_description="({rule_description}[^"]+)"""",
      """\srule_reason="({rule_reason}[^"]+)"""",
      """\strigger_type="({trigger_type}[^"]+)"""",
      """\strigger_entity="({trigger_entity}[^"]+)"""",
      """\surl="({url}[^"]+)"""",
      """\sevent_time="({event_time}\d{13})"""",
      """\slog_time="({log_time}\d{13})"""",
      """\sbase_risk_score="({base_risk_score}[\d.]+)"""",
      """\smitre_labels="({mitre_labels}[^"]+)"""",
      """\susecases="({rule_usecases}[^"]+)"""",
      """\sdomain="({domain}[^"]+)"""",
      """\shost="({host}[^"]+)"""",
      """\sdest_ip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
      """\sdest_host="({dest_host}[^"]+)"""",
      """\ssrc_ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """\ssrc_host="({src_host}[^"]+)"""",
      """\slabels="({asset_labels}[^"]+)"""",
      """\sincident_creation_time="({incident_creation_time}\d{13})"""",
      """\ssource_event_id="({event_id}[^"]+)"""",
      """\ssession_id="({session_id}[^"]+)""""
    ]
  

}
```
#### Parser Content
```Java
{
Name = exabeam-aa-kv-rule-trigger-success-anomaly
    ParserVersion = v1.0.0
    Vendor = Exabeam
    Product = Advanced Analytics
    TimeFormat = "epoch"
    log_timeFormat = "epoch"
    event_timeFormat = "epoch"
    incident_creation_timeFormat = "epoch"
    trigger_timeFormat = "epoch"
    Conditions = ["""exabeam-analytics-master""", """base_risk_score="""", """alert_source="anomaly"""", """trigger_type="""", """rule_name="""]
    Fields = [
      """\sincident_creation_time="({time}\d{13})"""",
      """\salert_source="({alert_source}anomaly)""""
      """\sid="({container_id}[^"]+)"""",
      """\sscore="({original_risk_score}\d+)"""",
      """\suser="(\*+|({user}[\w\.\-]{1,40}\$?))(\s*|")""",
      """\sevent_type="({event_category}[^"]+)"""",
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
      """\sdomain="({domain}[a-zA-z0-9.\-_]+(\.[a-zA-Z]{2,})?)"""",
      """\shost="({host}[\w\-.]+)"""",
      """\sdest_ip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F:]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
      """\sdest_host="({dest_host}[\w\-.]+)"""",
      """\ssrc_ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}(([0-9a-fA-F]){1,4})?)|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """\ssrc_host="({src_host}[\w\-.]+)"""",
      """\slabels="({asset_labels}[^"]+)"""",
      """\ssource_event_id="({event_id}[^"]+)"""",
      """\ssession_id="({session_id}[^"]+)""""
      """\sscore="({rule_severity}\d+)"""", 
    ]
    DupFields = [ "time -> incident_creation_time", "time -> trigger_time" ]
  

}
```
#### Parser Content
```Java
{
Name = exabeam-aa-kv-rule-trigger-success-anomaly
    ParserVersion = v1.0.0
    Vendor = Exabeam
    Product = Advanced Analytics
    TimeFormat = ["epoch", "yyyy-MM-dd'T'HH:mm:ss"]
    log_timeFormat = "epoch"
    event_timeFormat = "epoch"
    incident_creation_timeFormat = "epoch"
    event_from_time_millisFormat = "epoch"
    event_to_time_millisFormat   = "epoch"
    trigger_timeFormat = "epoch"
    Conditions = ["""exabeam-analytics-master""", """base_risk_score="""", """alert_source="anomaly"""", """trigger_type="""", """rule_name="""]
    Fields = [
      """timestamp="({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """\sincident_creation_time="({incident_creation_time}\d{13})"""",
      """\sincident_creation_time="({trigger_time}\d{13})"""",
      """\salert_source="({alert_source}anomaly)""""
      """\sid="({container_id}[^"]+)"""",
      """\sscore="({risk_score}\d+)"""",
      """\suser="({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """\sevent_type="({event_category}[^"]+)"""",
      """\srule_id="({rule_id}[^"]+)"""",
      """\srule_name="({rule}[^"]+)"""",
      """\srule_description="({rule_description}[^"]+)"""",
      """\srule_reason="({rule_reason}[^"]+)"""",
      """\strigger_type="({trigger_type}[^"]+)"""",
      """\strigger_entity="({trigger_entity}[^"]+)"""",
      """\surl="({url}[^"]+)"""",
      """\slog_time="({event_from_time_millis}\d{13})"""",
      """\slog_time="({event_to_time_millis}\d{13})"""",
      """\slog_time="({log_time}\d{13})"""",
      """\sbase_risk_score="({base_risk_score}[\d.]+)"""",
      """\susecases="({rule_usecases}[^"]+)""",
      """\sdomain="({domain}[a-zA-z0-9.\-_]+(\.[a-zA-Z]{2,})?)"""",
      """\shost="({host}[\w\-.]+)"""",
      """\sdest_ip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F:]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
      """\sdest_host="({dest_host}[\w\-.]+)"""",
      """\ssrc_ip="(({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
      """\ssrc_host="({src_host}[\w\-.]+)"""",
      """\slabels="({asset_labels}[^"]+)"""",
      """\ssource_event_({event_filter}[\w\=\-"]+)"""
      """\ssession_id="({session_id}[^"]+)""""
      """\sscore="({rule_severity}\d+)"""", 
      """app="({app}[^"=]+)""",
      """source="({log_source}[^"=]+)"""
      """mitre_labels="(({tactic_key}TA\d[^,"]+),\s*({tactic}[^,"]+)|({technique_key}T\d[^,"]+),\s*({technique}[^",]+))"""
      """mitre_labels="[^"]*?({tactic_key}TA[^,"]+)"""
      """mitre_labels="((TA\d[^,"]+),\s*({tactic}[^,"]+)|({technique_key}T\d[^,"]+),\s*({technique}[^",]+))"""
      """\ssource_event_id="({event_id}[^"]+)"""
      """\smitre_labels="({mitre_labels}[^"]+)"""",
      """\sevent_time="({event_time}\d{13})"""",
      """\sevent_time="({time}\d{13})"""",
      """\srawlog_time="({time}\d{13})"""",
      """\sweb_domain="({web_domain}[^"]+)"""",
      """\stop_domain="({top_domain}[^"]+)""""
      """rule_description="({observed_activity}[^"]+)"""
    ]
    DupFields = [  "risk_score -> original_risk_score" ]
  

}
```
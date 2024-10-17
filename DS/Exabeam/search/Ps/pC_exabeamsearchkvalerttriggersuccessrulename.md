#### Parser Content
```Java
{
Name = "exabeam-search-kv-alert-trigger-success-rulename"
    Vendor = "Exabeam"
    Product = "Search"
    TimeFormat = ["epoch", "yyyy-MM-dd'T'HH:mm:ss"]
    log_timeFormat = ["epoch"]
    Conditions = [
      """rule_name="""
      """rule_reason="""
      """event_type="""
      """mitre_labels="""
      """exabeam-analytics-master"""
    ]
    Fields = [
      """\Wevent_time="({time}\d{13})"""
      """timestamp="({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """query_key_value:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\|""",
      """\Wuser="({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
      """\Wdomain="({domain}[^"]+)"""
      """\Whost="({host}[\w.-]+)"""
      """\Wurl="({malware_url}[^"]+)"""
      """\Wrule_description="({rule_description}[^"]+)"""
      """\Wrule_id="({alert_id}[^"]+)"""
      """\Wscore="({original_risk_score}\d+)"""
      """\Wevent_type="({alert_type}[^"]+)"""
      """\Wrule_name="({alert_name}[^"]+)"""
      """\Wrule_reason="({rule_reason}[^"]+)"""
      """\Wsrc(_ip)?="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
      """\Wdest_ip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
      """\Wsrc_host="({src_host}[^"]+)"""
      """\Wdest_host="({dest_host}[^"]+)"""
      """\Wmitre_labels="({mitre_labels}[^"]+)""""
      """\Wusecases="({rule_usecases}[^"]+)""""
      """\Wevent_code="({event_id}[^"]+)""""
      """\Wrawlog_time="({log_time}[^"]+)""""
    ]
    DupFields = [
      "time->event_time", "rule_reason->alert_reason"
    ]
    SOAR {
      IncidentType = "ueba"
      DupFields = [
        "time->startedDate"
        "vendor->source"
        "rawLog->sourceInfo"
        "top_reasons->uebaRiskReasons"
        "user->uebaUserId"
        "original_score->uebaSessionRiskScore"
        "rule_description->description"
        "alert_severity->sourceSeverity"
        "alert_id->sourceId"
      ]
      NameTemplate = "Exabeam Alert ${alert_name} found"
      ProjectName = "SOC"
      EntityFields = [
        {
          EntityType = "user"
          Name = "windows_id"
          Fields = [
            "user->windows_id"
          ]
        

}
```
#### Parser Content
```Java
{
Name = "exabeam-search-kv-alert-trigger-success-rulealerts"
    Vendor = "Exabeam"
    Product = "Search"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = ["""exa_rule_name""", """exa_rule_category""", """exa_rule_id"""]
    Fields = [
      """(?:\W|")exa_rawEventTime(:|=)"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
      """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\s({host}[^\s]+)\sExabeam\s""",
      """query_key_value:\s+({user}[\w\.\-]{1,40}\$?)\s+\|""",
      """(?:\W|")user"*(:|=)\\?"*\s*({user}[\w\.\-]{1,40}\$?)\s*(?:\||\\?")""",
      """(?:\W|")host"*(:|=)\\?"*\s*({host}[^"|]+?)\s*(?:\||\\?")""",
      """(?:\W|")compare_key_value"*(:|=)"*\s*({additional_info}[^"|]+?)\s*(?:\||")""",
      """(?:\W|")cardinality_field_value"*(:|=)"*\s*({additional_info}[^"|]+?)\s*(?:\||")""",
      """(?:\W|")exa_rule_id"*(:|=)"*\s*({alert_id}[^"|]+?)\s*(?:\||")""",
      """(?:\W|")exa_rule_severity"*(:|=)"*\s*({alert_severity}[^"|]+?)(AlertSeverity)?\s*(?:\||")""",
      """(?:\W|")exa_rule_category"*(=|:)"*\s*({alert_type}[^"|]+?)\s*(?:\||")""",
      """(?:\W|")exa_rule_name"*(:|=)"*\s*({alert_name}[^"|]+?)\s*(?:\||")""",
      """(?:\W|")src(_ip)?"*(:|=)"*\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s*(?:\||"|\s+\w+=)""",
      """(?:\W|")dest_ip"*(:|=)"*\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s*(?:\||"|\s+\w+=)""",
      """(?:\W|")exa_link_logs"*(:|=)"*\s*({dl_exa_link_logs}[^"|]+?)\s*(?:\||")""",
      """(?:\W|")exa_link_alert"*(:|=)"*\s*({dl_exa_link_alert}[^"|]+?)\s*(?:\||")""",
      """(?:\W|")src_host"*(:|=)\\?"*\s*({src_host}[^"|]+?)\s*(?:\||\\?")""",
      """(?:\W|")dest_host"*(:|=)\\?"*\s*({dest_host}[^"|]+?)\s*(?:\||\\?")""",
      """exa_rule_description(:|=)"*({alert_reason}[^"\|=]+?)\s*(?:\||"|\s+\w+=)""",
      """exa_risk_score"*(:|=)"*\s*({original_risk_score}\d+?)\s*(?:\||")""",
      """(?:\W|")original_doc_message"*(=|:)\\?"*(\{({rule_description}[^\}]+)|\s*({=rule_description}[^"|]+?))\s*(?:\||\\?"|\})""",
      """\srule_description=\\?"({rule_description}[^"]+)"""",
      """exa_addRiskToUser(=|:)*"*({add_risk_to_user}\w+)""",
      """exa_addRiskToAsset(=|:)*"*({add_risk_to_asset}\w+)"""
    ]
    SOAR {
      IncidentType = "ueba"
      DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_reason->uebaRiskReasons", "dl_exa_link_alert->uebaSessionLink", "user->uebaUserId", "original_risk_score->uebaSessionRiskScore", "rule_description->description", "alert_severity->sourceSeverity", "alert_id->sourceId"]
      NameTemplate = """Exabeam Alert ${alert_name} found"""
      ProjectName = "SOC"
      EntityFields = [
        {EntityType = "device", Name = "src_address", Fields = ["src_ip->ip_address", "src_host->host_name"]

}
```
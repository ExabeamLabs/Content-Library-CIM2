#### Parser Content
```Java
{
Name = "exabeam-search-kv-alert-trigger-success-alertscount"
  Vendor = "Exabeam"
  Product = "Search"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
  """score="""
  """top_reasons="""
  """events_count="""
  """alerts_count="""
  ]
  Fields = [
  """\w+ \d+ \d\d:\d\d:\d\d\s({host}[^\s]+)"""
  """\sstart_time=\"({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2})"""
  """\sid=\"({session_id}[^\"]+)"""
  """\suser=\"({user}[^\"]+)"""
  """\sscore=\"({original_risk_score}\d+)"""
  """\sreasons_count=\"({reasons_count}\d+)"""
  """\sevents_count=\"({events_count}\d+)"""
  """\salerts_count=\"({alerts_count}\d+)"""
  """\surl=\"({session_url}[^\"]+)\""""
  """\szones=\"({network_zones}[^\"]+)\""""
  """\stop_reasons=\"(|({top_reasons}[^\"]*))\"*\s+\w+="""
  """\ssrc_ip=\"*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\ssrc_host=\"(|NA|-|({src_host}[^\"]*))\"*\s+\w+="""
  ]
  SOAR {
    IncidentType = "ueba"
    DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "top_reasons->uebaRiskReasons"
    "user->uebaUserId"
    "session_url->uebaSessionLink"
    "reasons_count->uebaRiskReasonsCount"
    "alerts_count->uebaAlertCount"
    "events_count->uebaEventCount"
    "network_zones->uebaNetworkZones"
    ]
    NameTemplate = "AA Session ${session_id} reported"
    ProjectName = "SOC"
    EntityFields = [
      {
        EntityType = "device"
        Name = "src_address"
        Fields = [
          """src_ip->ip_address"""
          """src_host->host_name"""
        ]
      

}
```
#### Parser Content
```Java
{
Name = "exabeam-search-kv-alert-trigger-success-alertscount"
    Vendor = "Exabeam"
    Product = "Advanced Analytics"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    end_timeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [
      """score="""
      """top_reasons="""
      """events_count="""
      """alerts_count="""
    ]
    Fields = [
      """\w+ \d+ \d\d:\d\d:\d\d\s({host}[^\s]+)"""
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\sexabeam-analytics-master""" 
      """timestamp="({time}[^"]+)"""", 
      """\sid=\"({session_id}[^\"]+)"""
      """\suser=\"({user}[\w\.\-]{1,40}\$?)"""
      """\sscore=\"({original_risk_score}\d+)"""
      """\sreasons_count=\"({reasons_count}\d+)"""
      """\sevents_count=\"({events_count}\d+)"""
      """\salerts_count=\"({alerts_count}\d+)"""
      """\surl=\"({url}[^\"]+)\""""
      """\szones=\"({network_zones}[^\"]+)\""""
      """\stop_reasons=\"(|({alert_reason}[^\"]*))\"*\s+\w+="""
      """\ssrc_ip=\"*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """\ssrc_host=\"(|NA|-|({src_host}[^\"]*))\"*\s+\w+=""",
      """end_time=\"({end_time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
      """labels=\"({asset_labels}[^\"]+)\""""
    ]
    SOAR {
      IncidentType = "ueba"
      DupFields = [
        "time->startedDate"
        "vendor->source"
        "rawLog->sourceInfo"
        "alert_reason->uebaRiskReasons"
        "user->uebaUserId"
        "url->uebaSessionLink"
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
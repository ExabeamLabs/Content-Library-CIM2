#### Parser Content
```Java
{
Name = "pan-ngfw-csv-alert-trigger-success-url"
Vendor = "Palo Alto Networks"
Product = "Palo Alto NGFW"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy/MM/dd HH:mm:ss"]
Conditions = [
  """,THREAT,url,"""
  """,malware,"""
]
Fields = [
  """\s+({host}[^\s]+)\s+\d+,.+?,.+?,THREAT,"""
  """THREAT,[^,]+,\d+,(|({time}\d+/\d+/\d+\s+\d\d:\d\d:\d\d)),({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),([^,]*?,){15}(|({src_port}\d+)),(|({dest_port}\d+)),([^,]*?,){3}(|({protocol}[^,]+?)),(|({alert_type}[^,]+?)),"*({malware_url}[^<]+?)"*,(9999)?\(9999\),[^,]+?,({alert_severity}[^,]+?),({additional_info}[^,]+),({alert_id}\d+)"""
  """,THREAT,([^,]*?,){8}(?:\w+\\)?((({user}[\w\.\-]{1,40}\$?)@({domain}[^",]+(\.prd)?))|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({=user}[\w\.\-]{1,40})))"""
  """,THREAT,([^,]*?,){9}(?:\w+\\)?((({user}[\w\.\-]{1,40}\$?)@({domain}[^",]+(\.prd)?))|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({=user}[\w\.\-]{1,40})))"""
  """\(9999\),([^,]*,){13}(("({user_agent}[^"]+)")|({=user_agent}[^,]+)),"""
  """\(9999\),({alert_name}[^,]+),"""
  """THREAT,url,([^,]*,){26}("+)?.*?({web_domain}[^\/\.\s]+(?i)(\.(com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ai|ms|mx))+)[\\\/\s:"]"""
  """,(any|({category}[^,]+?)),Informational,client to server,""",
  """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
]
SOAR {
  IncidentType = "malware"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "alert_name->malwareName"
    "alert_id->sourceId"
    "alert_severity->sourceSeverity"
    "src_ip->malwareVictimHost"
    "alert_type->malwareCategory"
    "alert_id->sourceId"
    "alert_severity->sourceSeverity"
    "src_ip->malwareVictimHost"
    "alert_type->malwareCategory"
    "malware_url->malwareAttackerUrl"
    "dest_ip->malwareAttackerIp"
  ]
  NameTemplate = "Palo Alto Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "dest_address"
      Fields = [
        "dest_ip->ip_address"
      ]
    

}
```
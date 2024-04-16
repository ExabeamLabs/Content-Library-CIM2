#### Parser Content
```Java
{
Name = netskope-sc-json-alert-trigger-success-dlp
  Product = Netskope Security Cloud
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"alert_type":"DLP"""", """"alert":"yes"""", """"src-application-name":"Netskope"""", """"triggered-by":""" ]
  Fields = ${NetskopeParsersTemplates.cef-netskope-alert.Fields}[
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
    """"app":"({app}[^"]+)"""",
    """"_id":"({alert_id}[^"]+)"""",
    """"category":"({threat_category}[^"]+)"""",
    """"md5":"({hash_md5}[^"\s]+)"""",
    """"dlp_rule_severity":"({alert_severity}[^"]+)"""",
    """"alert_type":"({alert_name}[^"]+)"""",
    """"type":"({alert_type}[^"]+)"""",
    """"policy":"({additional_info}[^"]+)"""",
    """"action":"({result}[^"]+)"""",
    """"object":"({email_subject}[^"]+?)\s*"""",
    """"file_size":({bytes}\d+)""",
    """"mime_type":"({mime}[^"]+)""""
  ]

cef-netskope-alert = {
  Vendor = Netskope
  TimeFormat = "epoch_sec"
  Fields = [
    """"hostname":"({host}[^",]+)"""",
    """"timestamp":({time}\d{10})""",
    """"user":"(({email_address}[^@"\s]+@[^@"\s]+\.[^"\s]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[\w\.\-]{1,40}\$?))"""",
    """"dstip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"alert_name":"({alert_name}[^"]+)""",
    """"url":"({malware_url}[^"]+)""",
    """"userip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  SOAR {
    IncidentType = "malware"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->malwareName", "src_host->malwareVictimHost", "alert_type->description", "malware_url->malwareAttackerUrl"]
    NameTemplate = """Netskope Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]},
      {EntityType="user", Name ="windows_id", Fields=["user->windows_id"]},
    
}
```
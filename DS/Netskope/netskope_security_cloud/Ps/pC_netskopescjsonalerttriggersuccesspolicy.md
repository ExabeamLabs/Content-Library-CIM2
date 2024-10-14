#### Parser Content
```Java
{
Name = netskope-sc-json-alert-trigger-success-policy
  Product = Netskope Security Cloud
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"alert_type":"policy"""", """src-application-name":"Netskope""", """"alert":"yes"""", """"alert_name":""" ]
  Fields = ${NetskopeParsersTemplates.cef-netskope-alert.Fields}[
    """"time":"({time}[^"]+)""""
    """"srcip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"alert_type":"({alert_type}[^"]+)""",
    """"action":"({result}[^"]+)""",
    """"hostname":"({src_host}[\w.-]+)"""",
    """"referer":"({referrer}[^"]+)""",
    """"policy":"({additional_info}[^"]+)""",
    """"page":"({web_domain}[^\\\/"]+)""",
    """"severity":({alert_severity}[^,"]+)""",
    """"_id":"({alert_id}[^"]+)""",
    """"file_path":"({file_path_at}[^"]+)"""",
    """"site":"({site_at}[^"]+)""""
  ]
  ParserVersion = v1.0.0

cef-netskope-alert = {
  Vendor = Netskope
  TimeFormat = "epoch_sec"
  Fields = [
    """"hostname":"({host}[^",]+)"""",
    """"timestamp":({time}\d{10})""",
    """"user":"(({email_address}[^@"\s]+@[^@"\s]+\.[^"\s]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
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
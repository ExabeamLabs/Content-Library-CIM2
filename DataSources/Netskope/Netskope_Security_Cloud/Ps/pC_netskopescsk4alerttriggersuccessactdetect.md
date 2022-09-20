#### Parser Content
```Java
{
Name = netskope-sc-sk4-alert-trigger-success-actdetect
  ParserVersion = v1.0.0
  Product = Netskope Security Cloud
  Conditions = [ """"alert_type":"policy"""", """destinationServiceName =Netskope""", """"alert":"yes"""", """act=detect""" ]
  Fields = ${NetskopeParsersTemplates.cef-netskope-alert.Fields}[
    """"srcip":"({src_translated_ip}[A-Fa-f:\d.]+)""",
    """"malsite_category":\["({threat_category}[^"]+)"[^\]]*?\]""",
    """"alert_type":"({alert_type}[^"]+)""",
    """"action":"({action}[^"]+)""",
    """"hostname":"({src_host}[^"]+)""",
    """"referer":"({referrer}[^"]+)""",
    """"policy":"({additional_info}[^"]+)""",
    """"page":"({web_domain}[^\\\/"]+)""",
    """CEF:([^\|]*\|){6}({alert_severity}[^\|]+)\|""",
    """"_id":"({alert_id}[^"]+)""",
    """"file_path":"({file_path_at}[^"]+)"""",
    """"site":"({site_at}[^"]+)""""
  ]

cef-netskope-alert = {
  Vendor = Netskope
  TimeFormat = "epoch_sec"
  Fields = [
    """"hostname":"({host}[^",]+)"""",
    """"timestamp":({time}\d+)""",
    """"user":"(({email_address}[^@"\s]+@[^@"\s]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[^"@\\\/\s]+))"""",
    """"dstip":"({dest_ip}[A-Fa-f:\d.]+)""",
    """"alert_name":"({alert_name}[^"]+)""",
    """"url":"({malware_url}[^"]+)""",
    """"userip":"({src_ip}[A-Fa-f:\d.]+)"""
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
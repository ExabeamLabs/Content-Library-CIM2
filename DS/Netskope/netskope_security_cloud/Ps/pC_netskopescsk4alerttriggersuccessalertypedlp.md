#### Parser Content
```Java
{
Name = netskope-sc-sk4-alert-trigger-success-alertypedlp
  ParserVersion = v1.0.0
  Vendor = "Netskope"
  Product = "Netskope Security Cloud"
  TimeFormat = "epoch_sec"
  Conditions = [ """"alert_type":"DLP"""", """destinationServiceName =Netskope""", """"alert_name":"""", """"alert":"yes""""  ]
  Fields = [
    """"hostname":"({host}[^",]+)"""",
    """"timestamp":({time}\d{10})""",
    """requestClientApplication=({app}[^=]+?)\s+(\w+=|$)"""
    """"app":\s*"\[?({app}[^\"\]]+)"""
    """"dstip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"alert_name":"({alert_name}[^"]+)""",
    """"srcip":\s*"({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\""""
    """"userip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """"user":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)(?<!local)(?<!loc)(?<!localdomain)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"user":\s*"(unknown|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)(?<!local)(?<!loc)(?<!localdomain)|(({domain}[^\s\"@\\\/]+)[\\\/]+)?(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({user}[\w\.\-\!\#\^\~]{1,40}\$?))))""""
    """"object":\s*"(\s+\"|(\s*(Unknown Unknown|unknown|Unknown|null|({object}[^\"]+?))\s*\"))"""
    """"access_method":\s*"({auth_method}[^\"]+)"""
    """"logintype":\s*"({auth_method}[^\"]+)"""
    """"activity":\s*"({operation}[^\"]+)"""
    """"os":\s*"((U|u)nknown|({os}[^\"]+))"""
    """"browser":\s*"((U|u)nknown|({browser}[^\"]+))"""
    """"page":\s*"({web_domain}[^\"\/]+)"""
    """"dst_location":\s*"(N/A|({location}[^\"]+))"""
    """"file_size":\s*({bytes}\d+)"""
    """"file_type":\s*"({file_type}[^"]+)"""
    """"page_site":\s*"({app}[^\"]+)"""
    """"dstport\":"\s*({dest_port}\d+)""""
    """"url":"({malware_url}[^"]+)""",
    """"url":\s*"({url}[^\"]+)"""
    """"action\":"({action}[^\"]+)"""
    """"app":"({app}[^"]+)""",
    """"dlp_incident_id":({alert_id}\d+)""",
    """"_id":"({alert_id}[^"]+)""",
    """"category":"({threat_category}[^"]+)""",
    """"md5":"({hash_md5}[^"\s]+)"""",
    """"dlp_rule_severity":"({alert_severity}[^"]+)""",
    """"alert_type":"({alert_type}[^"]+)""",
    """"policy":"({additional_info}[^"]+)""",
    """"action":"({action}[^"]+)""",
    """"*hostname"*:"*({src_host}[^"]+)"""",
    """"from_user":"({from_user_at}[^"]+)"""",
    """shared_with":"({shared_with_at}[^"]+)""",
    """"sha256":"({hash_sha256_at}[^"]+)"""",
    """"site":"({site_at}[^"]+)""""
    """"policy":"({alert_name}[^"]+)""",
    """"referer":"({referrer}[^"]+)"""",
    """"dlp_incident_id":({alert_id}\d+)"""
    """"severity":"({alert_severity}[^,"]+)"""
    """msg[^\[:,\.]+\[({alert_source}[^]]+)"""
    """"protocol":"({protocol}[^"]+)""""
    ]
  DupFields = [ "object->file_name", "host->src_host","operation->alert_type"]

SOAR {
    IncidentType = "malware"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->malwareName", "src_host->malwareVictimHost", "alert_type->description", "malware_url->malwareAttackerUrl"]
    NameTemplate = """Netskope Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]

}
```
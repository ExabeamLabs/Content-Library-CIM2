#### Parser Content
```Java
{
Name = netskope-sc-sk4-alert-trigger-success-actdetect
  ParserVersion = v1.0.0
  Product = Netskope Security Cloud
  Conditions = [ """"alert":"yes"""", """"object_type":""", """"ccl":""", """"action":""", """"access_method":""" ]
  Fields = ${NetskopeParsersTemplates.cef-netskope-alert.Fields}[
    """"srcip":"({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """"malsite_category":\["({threat_category}[^"]+)"[^\]]*?\]""",
    """"type":"({alert_type}[^"]+)"""
    """"category":"(n\/a|({alert_type}[^"]+))"""
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
    """ fileHash=({hash_md5}[^=]+?)\s+\w+=""",
    """"category":"({category}[^"]+?)"""",
    """"malware_id"+:"+({alert_id}[^"]+)""",
    """"malware_name":"({malware_file_name}[^"]+?)"""",
    """msg=({additional_info}[^=]+?)\s+\w+=""",
    """dpriv=({alert_type}[^=]+?)\s\w+=""",
    """"malware_type"+:"+({alert_name}[^"]+)"""",
    """"+malware_sev"+:"+({alert_severity}[^"]+)""",
    """suser=(({email_address}[^@"\s]+@({email_domain}[^@"\s]+))|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[\w\.\-]{1,40}\$?))"""
    """msg[^\[:,\.]+\[({alert_source}[^]]+)"""
    """"protocol":"({protocol}[^"]+)"""",
    """"activity":\s*"({operation}[^\"]+)""",
    """"access_method":\s*"({auth_method}[^\"]+)"""
    """"logintype":\s*"({auth_method}[^\"]+)""",
    """"alert":"({alert_status}[^",]+)""",
    """"app":\s*"\[?({app}[^\"\]]+)""",
    """"object":"({object}[^"]+)"""
    """"object":\s*"'?\s*({file_name}[^"]+?(\.({file_ext}[^"\.\s\\\/]+?))?)'?"[^\}]*?"object_type":\s*"(File|Image)"""",
    """"object":\s*"'?\s*(({folder_name}[^"\\\/']+)|({file_dir}[^"\/\\']+[\/\\]+[^"]+))"'?[^\}]*?"object_type":\s*"Folder"""",
    """"object":\s*"({file_name}[^"\\\/]+?(\.({file_ext}[^"\.\s\\\/]+?))?)"[^\}]*?"activity":\s*"File\w+"""",
    """"object_type":\s*"(File|Image)"[^\}]*?"object":\s*"\s*({file_name}[^"]+?(\.({file_ext}[^"\.\s\\\/]+?))?)""""
    """"useragent":"({user_agent}[^"]+)"""",
    """"os":\s*"((U|u)nknown|({os}[^\"]+))""",
    """"browser":\s*"((U|u)nknown|({browser}[^\"]+))""",
    """"page":\s*"({web_domain}[^\"\/]+)""",
    """"url":\s*"({url}[^\"]+)""",
    """"dst_location":\s*"(N/A|({location}[^\"]+))""",
    """"activity":\s*"File\w+"[^\}]*?"object":\s*"({file_name}[^"\\\/]+?(\.({file_ext}[^"\.\s\\\/]+?))?)"""",
    """"shared_with":"({shared_with_at}[^"]+)"""",
    """"policy":"({policy_name}[^"]+)"""

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
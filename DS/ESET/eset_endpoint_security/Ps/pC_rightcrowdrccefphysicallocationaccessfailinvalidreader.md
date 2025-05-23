#### Parser Content
```Java
{
Name = "rightcrowd-rc-cef-physical-location-access-fail-invalidreader"
Conditions = [
"""CEF:"""
"""|RightCrowd|RightCrowd|"""
"""|Invalid reader|"""
"""eventId="""
]
ParserVersion = "v1.0.0"

eset-activity.Fields}[
    """eventDesc=({alert_name}[^=]+?)\s*(\w+=|$)""",
    """scannerID=({additional_info}[^=]+?)\s*(\w+=|$)""",
    """\Wsev=({alert_severity}\d+)"""
  ]
  DupFields = ["event_name->alert_type"]
  ParserVersion = "v1.0.0"
},

 {
    Name = eset-es-leef-alert-trigger-success-threatevent
    Vendor = ESET
    Product = ESET Endpoint Security
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Conditions = [ """LEEF:""", """|ESET|RemoteAdministrator|""","""cat=ESET Threat Event""","""threatType=""" ]
    Fields = [
      """deviceName =({host}[^\s]+)\s""",
      """\Wcat=({threat_category}[^=]+?)\s*(\w+=|$)""",
      """\Wsev=({alert_severity}\d+)""",
      """\WdevTime=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
      """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """threatType=({alert_type}[^=]+?)\s*(\w+=|$)""",
      """\|ESET\|(?:[^\|]+\|){2}({alert_type}[^\|]+)""",
      """threatName =({alert_name}[^=]+?)\s*(\w+=|$)""",
      """eventDesc=({alert_name}[^=]+?)\s*(\w+=|$)""",
      """objectUri=({malware_url}[^=]+?)\s*(\w+=|$)""",
      """actionTaken=({action}[^=]+?)\s*(\w+=|$)""",
      """accountName =((({domain}[^\\=]+?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*(\w+=|$)""",
      """engineVersion=({engine_version}\d+)""",
      """objectType=({object_type}[^=]+?)\s*(\w+=|$)""",
      """threatHandled=({threat_handled}\d+)""",
      """needRestart=({result_code}\d+)""",
      """circumstances=({circumstances}[^=]+?)\s*(\w+=|$)""",
      """firstseen=({firstseen}[^=]+?)\s*(\w+=|$)""",
      """hash=({hash_sha256}[^\s]+)"""
    ]
    DupFields = ["action->additional_info", "host->dest_host", "malware_url->process_name"]
	ParserVersion = "v1.0.0"
  },

{
  Name = tenable-t-json-alert-trigger-success-dcerpcservice
  ExtractionType = json
  Vendor = Tenable
  Product = Tenable Web App Scanning
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"scan":""", """"completed_at":""", """"synopsis":""",""""IO_address":""", """"asset_fqdn":""", """"publication_date":""" ]
  Fields = [
    """exa_json_path=$.scan.started_at,exa_field_name=time"""
    """exa_json_path=$.asset_fqdn,exa_field_name=host"""
    """exa_json_path=$.ipv4,exa_field_name=src_ip"""
    """exa_json_path=$.severity,exa_field_name=alert_severity"""
    """exa_json_path=$.plugin.name,exa_field_name=alert_name"""
    """exa_json_path=$.plugin.description,exa_field_name=additional_info"""
    """exa_json_path=$.plugin.vpr..cvss3_impact_score,exa_field_name=original_risk_score"""
    """exa_json_path=$.plugin.vpr..exploit_code_maturity,exa_field_name=exploit_code_maturity"""
    """exa_json_path=$.plugin.see_also,exa_field_name=see_also"""
    """exa_json_path=$.plugin.cve,exa_field_name=cve_id"""
    """exa_json_path=$.port.protocol,exa_field_name=protocol"""
    """exa_json_path=$.state,exa_field_name=action"""
    """exa_json_path=$.plugin.solution,exa_field_name=solution"""
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = tenable-t-sk4-alert-trigger-success-dcerpcservice-1
  Vendor = Tenable
  Product = Tenable Web App Scanning
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"scan":""", """"completed_at":""", """"synopsis":""", """fqdn":""", """"publication_date":""" ]
  Fields = [
    """started_at"+:\s*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """"hostname"+:\s*"+({host}[^"]+)""",
    """"+ipv4"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"+severity"+:\s*"+({alert_severity}[^"]+)""",
    """"name"+:\s*"+({alert_name}[^"]+)""",
    """"+description"+:\s*"+({additional_info}[^"]+?)"+""",
    """cvss_base_score"+:\s*({cvss_base_score}[^,]+)""",
    """cvss3_impact_score"+:\s*({original_risk_score}\d+)""",
    """exploit_code_maturity"+:\s*"+({exploit_code_maturity}[^"]+)""",
    """see_also"+:\s*\["*(|({see_also}[^\]]+?))"*\]""",
    """cve"+:\s*\[({cve_id}[^\]]+)\]""",
    """protocol"+:\s*"+({protocol}[^"]+)""",
    """"state"+:\s*"+({action}[^"]+)""",
    """"solution"+:\s*"+((?i)n\/a|({solution}[^"]+))"""
  ]
  ParserVersion = "v1.0.0"
},

{
Vendor = Netwrix
Product = Netwrix Auditor
TimeFormat = "MMM dd yyyy HH:mm:ss"
Fields = [
  """start=({time}\w{3} \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
  """suser=(N\/A|({email_address}[^@]+@[^\\\s]+)|(({domain}[^\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)) """
  """shost=(unknown|({src_host}[^\s]+))"""
  """({app}Netwrix)"""
  """msg=({additional_info}.+?)(\s\w+=|$)"""
  """CEF:0\|Netwrix\|Self-audit\|[^\|]+\|[^\|]+\|({operation}[^\|]+)\|"""
  """cat=({object_type}.+?) \w+=.+?filePath=({object}.+?) \w+="""
]
Name = netwrix-auditor-cef-app-activity-success-settingschanged
Conditions = [
  """CEF:0|Netwrix|Self-audit|"""
]
ParserVersion = "v1.0.0"
},

{
Name = barracuda-esg-cef-email-receive-barracudanetworks
Vendor = "Barracuda"
Product = "Barracuda Email Security Gateway"
TimeFormat = "epoch"
Conditions = [
  """Barracuda Networks"""
  """Email Security Gateway"""
]
Fields = [
  """dvc=({host}[^\s]+)"""
  """\srt=({time}\d{13})""" 
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """act=({action}[^\s]+)"""
  """flexString1=({operation}[^\:]+):({result}\d+)"""
  """\|({alert_severity}[^\|]+)\|\s*event"""
  """suser=(-|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"""
  """duser=(-|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"""
  """reason=({alert_name}\d+)"""
]
ParserVersion = "v1.0.0"
},

{
Name = forcepoint-emailsecurity-cef-email-send-success-message
Vendor = "Forcepoint"
Product = "Forcepoint Email Security"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|Forcepoint|Email Security|"""
  """msg="""
]
Fields = [
  """\Wmsg=({email_subject}[^=]+?)\s+\w+="""
  """\Wmsg=\[({email_subject}[^\]]+)"""
  """\Win=({bytes}\d+)"""
  """\Wrt=({time}\d{13})"""
  """\WtrueSrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wdvc=(ConnectorIP|({host}[a-fA-F\d.:]+))"""
  """\Wdvchost=({host}[^\s]+)"""
  """\WmessageId=({alert_id}[^\s]+)"""
  """\|Forcepoint\|Email Security\|[^\|]*\|({alert_name}[^\|]*)\|({alert_type}[^\|]*)\|({alert_severity}[^\|]*)\|"""
  """suser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(>)?(\s|\s*$)"""
  """\Wsuser=\s*([^<]+<)?(<)?({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(>)?(\s+\w+=|\s*$)"""
  """duser=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(>)?(\s|\s*$)"""
  """\Wduser=\s*([^<]+<)?(<)?({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(>)?(\s+\w+=|\s*$)"""
  """ad.fnameAndfileHash=({email_attachments}[^|]+?)\s*\|\s*({file_hash}[^|\s]+)"""
  """ad.cc=\s*(Email_in_CC|({email_recipients}[^=]+))\s+[\w.\-]+="""
]
ParserVersion = "v1.0.0"
},


${HornetDlpEmailTemplates.hornet-dlp-email}{
  Name = hornet-email-kv-email-receive-success-1
  Conditions = [ """main_domain=""", """owner=""", """smtp_code=""", """crypt_type=""", """from_hdr=""", """update_nr=""", """type=1""" ]
  ParserVersion = "v1.0.0"
},

{
  Name = hornet-email-kv-alert-trigger-success-5
  ParserVersion = v1.0.0
  Vendor = Hornet
  Product = Hornetsecurity Cloud Email Security Services
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """main_domain=""", """owner=""", """smtp_code=""", """crypt_type=""", """from_hdr=""", """update_nr=""", """type=5""" ]
  Fields = [
    """date=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """reason="({alert_name}[^"]+)""",
    """type=({alert_type}5)""",
    """msgid="({alert_id}[^"]+)""",
    """dir=({direction}1|2)""",
    """main_domain=({domain}[^=]+?)\s*(\w+=|$)""",
    """from=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """to=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """src_host=((?i)unknown|({src_host}[^\s]+))""",
    """src_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dst_ip=(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^\s]+))""",
    """attachments="[^0"]#({email_attachments}[^"]+)""",
    """subject="[ \s]*({email_subject}[^"]+?)[ \s]*"""",
  ]
  DupFields = [ "alert_type->alert_severity" 
}
```
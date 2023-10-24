#### Parser Content
```Java
{
Name = sentinelone-singularityp-cef-alert-trigger-threatclassification
    Vendor = SentinelOne
    Product = Singularity Platform
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ "CEF:", "|SentinelOne", "|threatClassification=", "|threatDetectingEngine=", "|threatClassifier=" ]
    Fields = [
      """CEF:([^\|]*\|){5}({alert_name}[^\|]+)""",
      """\WdeviceAddress=({host}[^\|]+?)((\||\s+)\w+=|\s*$)""",
      """\WdeviceHostName =({host}[^\|]+?)((\||\s+)\w+=|\s*$)""",
      """\WoriginatorName =({src_host}[^\|]+?)((\||\s+)\w+=|\s*$)""",
      """\WeventDesc=({alert_name}[^\|]+?)(\s+-\s+({src_host}[^\|]+?))?((\||\s+)\w+=|\s*$)""",
      """\WeventSeverity=({alert_severity}[^\|]+?)((\||\s+)\w+=|\s*$)""",
      """\Wrt=[^=\|]*?({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
      """\Wrt=({time}\w+, \d\d \w+ \d\d\d\d, \d\d:\d\d:\d\d \w+)""",
      """\Wrt=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """\WfileHash=(N/A|({hash_md5}[^\|]+?))((\||\s+)\w+=|\s*$)""",
      """\WfilePath=(N/A|({file_path}[^\|]+?))((\||\s+)\w+=|\s*$)""",
      """\WfileName =({file_dir}[^\|]*?\\(({user}[\w\.\-]{1,40}\$?)\\Desktop\\)?)({file_name}[^\\\|]+?({file_ext}[^\\\|\.]+)?)((\||\s+)\w+=|\s*$)""",
      """\WthreatClassification=({alert_name}[^\|]+?)((\||\s+)\w+=|\s*$)""",
      """\WthreatID=({alert_id}[^\|]+?)((\||\s+)\w+=|\s*$)""",
      """\WsourceNetworkState=({src_net_status}[^\|]+?)((\||\s+)\w+=|\s*$)""",
      """\WsourceOsRevision=({os_revision}[^\|]+?)((\||\s+)\w+=|\s*$)""",
      """\WsourceOsType=({src_host_type}[^\|]+?)((\||\s+)\w+=|\s*$)""",
      """\WsourceFqdn=({src_fqdn}[^\|]+?)((\||\s+)\w+=|\s*$)""",
      """\WsourceDnsDomain=({src_domain}[^\|]+?)((\||\s+)\w+=|\s*$)""",
      """\WsourceHostName =({src_host}[^\|]+?)((\||\s+)\w+=|\s*$)""",
      """\WsourceAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?((\||\s+)\w+=|\s*$)""",
      """\WsourceNetInterfaceName =({src_interface}[^\|]+?)((\||\s+)\w+=|\s*$)""",
      """\WsourceMacAddress=({src_mac}[^\|]+?)((\||\s+)\w+=|\s*$)""",
      """\Wcat=(|({category}.+?))(\s+\w+=|\s*$)""",
      """\Wuuid=(|({user_uid}.+?))(\s+\w+=|\s*$)""",
      """\WactivityID=(|({activity_id}.+?))(\s+\w+=|\s*$)""",
      """\WactivityType=(|({operation_type}.+?))(\s+\w+=|\s*$)""",
      """\WaccountId=(|({account_id}.+?))(\s+\w+=|\s*$)""",
      """\WaccountName =(|({account_name}.+?))(\s+\w+=|\s*$)""",
# notification_scope is removed
    ]
  ParserVersion = "v1.0.0"
  

}
```
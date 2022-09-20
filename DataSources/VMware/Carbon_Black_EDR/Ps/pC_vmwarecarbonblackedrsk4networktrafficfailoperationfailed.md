#### Parser Content
```Java
{
Name = vmware-carbonblackedr-sk4-network-traffic-fail-operationfailed
  ParserVersion = v1.0.0
  Product = Carbon Black EDR
  Conditions = [ """threatIndicators""" , """ The operation failed""", """eventType=NETWORK""", """destinationServiceName =CB Defense""" ]
  Fields = ${CarbonBlackParsersTemplates.cef-carbonblack-events-1.Fields} [
    """({result}failed)""",
  ]

cef-carbonblack-events-1 {
  Vendor = VMware
  TimeFormat = "epoch"
  Fields = [
    """"eventTime":({time}\d+),""",
    """"deviceIpAddress":"({src_ip}[a-fA-F:\d.]+)"""",
    """"deviceName":"(({web_domain}[^\\\s"]+)\\{1,20})?({src_host}[^\\\s"]+)"""",
    """"email":"(({email_domain}[^\\"]+)\\+)?(HiveStreamingService|SYSTEM|({user}[^\s"@]+))"""",
    """"eventType":"({alert_name}[^"]+)"""",
    """"applicationName":"({process_name}[^"]+)"""",
    """"targetPriorityType":"({alert_severity}[^"]+)"""",
    """"eventType":"({alert_type}[^"]+)"""",
    """"threatIndicators":\[?"({alert_type}[^"]+)"""",
    """"applicationPath":"({process_path}(({process_dir}[^"=,]+?)[\\\/]+)?({process_name}[^\/\\"]+))"""",
    """"peerFqdn":"(::|({web_domain}[^"]+))"""",
    """"peerFqdn":"[^"\s]*?({top_domain}[^\/\.\s"]+(?i)(\.(com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za))+)""",
    """"destAddress":"({dest_ip}[a-fA-F\d:.]+)"""",
    """"name":"({file_path}(\w:|\\\\)[^"]+)"""",
    """"name":"({file_name}[^\\\/"]+?(\.({file_ext}[^"]+))?)"""",
    """"name":"({file_dir}(\w:|\\\\)[^"]+?)\\+(?:[^\\"]+?)"""",
    """>\s*({file_name}[^<"']+?)<\/link><\/share>"*\s*was created by the application""",
    """"name":"({file_path}(({file_dir}\w+:[^"]+?)\\+)\s*({file_name}[^"\\,:]+?))"""",
    """"eventId":"({alert_id}[^"]+)"""",
    """"parentApp":\{[^}]+"md5Hash":"({parent_md5hash}[^"]+)""",
    """"parentApp":\{[^}]+"sha256Hash":"({parent_sha256}[^"]+)"""",
    """"targetApp":\{[^}]+"sha256Hash":"({target_hash_sha256}[^"]+)"""",
    """"targetApp":\{[^}]+"md5Hash":"({target_md5hash}[^"]+)"""",
    """"selectedApp":\{[^}]+"md5Hash":"({selected_md5hash}[^"]+)"""",
    """"selectedApp":\{[^}]+"sha256Hash":"({selected_hash_sha256}[^"]+)"""",
  
}
```
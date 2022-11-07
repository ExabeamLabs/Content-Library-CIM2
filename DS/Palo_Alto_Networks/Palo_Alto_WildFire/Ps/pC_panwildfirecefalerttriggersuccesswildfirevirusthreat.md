#### Parser Content
```Java
{
Name = pan-wildfire-cef-alert-trigger-success-wildfirevirusthreat
  TimeFormat = "MMM dd yyyy HH:mm:ss zzz"
  Conditions = [ """|Palo Alto Networks|PAN-OS|""","""wildfire-virus|THREAT|""" ]
  ParserVersion = "v1.0.0"

pan-cef-alert = {
  Vendor = Palo Alto Networks
  Product = Palo Alto WildFire
  TimeFormat = "epoch"
  Fields = [
    """\|Palo Alto Networks\|PAN-OS\|[^|]+?\|({alert_type}.+?)\|THREAT\|""",
    """\|Palo Alto Networks\|PAN-OS\|[^|]+?\|[^|]+?\|THREAT\|({alert_severity}.+?)\|""",
    """cat=(|({alert_name}.+?))(\s+\w+=|\s*$)""",
    """\Wproto=(|({protocol}.+?))(\s+\w+=|\s*$)""",
    """\Wapp=(|({process_name}.+?))(\s+\w+=|\s*$)""",
    """\Wact=(|({action}.+?))(\s+\w+=|\s*$)""",
    """\sflexString2=({additional_info}[^\s]+)""",
    """\Wcs1=(|({additional_info}.+?))(\s+\w+=|\s*$)""",
    """\sexternalId=({alert_id}[^\s]+)""",
    """\Wrt=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d \w+)""",
    """\srt=({time}\d+)""",
    """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """duser=(({domain}[^\\=]+)\\+)?({user}[^\s@]+)(@({=domain}[^\s@=]+))?""",
    """suser=(({domain}[^\\=]+)\\+)?({user}[^\s@]+)(@({=domain}[^\s@=]+))?""",
    """\ssourceTranslatedAddress=({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdestinationTranslatedAddress=({dest_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdvchost=({host}[^\s]+)""",
    """\srequest="({malware_url}.+?)"\s""",
    """\sspt=({src_port}\d+)""",
    """\sdpt=({dest_port}\d+)""",
  ]
  DupFields = [ "alert_type->category" 
}
```
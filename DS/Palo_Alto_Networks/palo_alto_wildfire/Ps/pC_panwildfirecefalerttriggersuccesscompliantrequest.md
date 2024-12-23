#### Parser Content
```Java
{
Name = pan-wildfire-cef-alert-trigger-success-compliantrequest
  TimeFormat = "MMM dd yyyy HH:mm:ss zzz"
  Conditions = [ """Palo Alto Networks|PAN-OS|""","""HTTP Non-RFC Compliant Request(39143)|THREAT|""" ]
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
    """\Wact=(|({result}.+?))(\s+\w+=|\s*$)""",
    """\sflexString2=({additional_info}[^\s]+)""",
    """\Wcs1=(|({additional_info}.+?))(\s+\w+=|\s*$)""",
    """\sexternalId=({alert_id}[^\s]+)""",
    """\Wrt=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d \w+)""",
    """\srt=({time}\d{13})""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """duser=(({domain}[^\\=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({=domain}[^\s@=]+))?""",
    """suser=(({domain}[^\\=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({=domain}[^\s@=]+))?""",
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
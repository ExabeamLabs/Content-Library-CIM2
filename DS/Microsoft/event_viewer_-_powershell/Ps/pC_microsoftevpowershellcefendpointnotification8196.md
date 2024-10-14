#### Parser Content
```Java
{
Name = microsoft-evpowershell-cef-endpoint-notification-8196
  ParserVersion = "v1.0.0"
  Product = Event Viewer - PowerShell
  Conditions = [ """CEF: """, """|Microsoft|PowerShell|""", """|Microsoft-Windows-PowerShell:8196|""" ]

microsoft-windows-cef-powershell = {
  Vendor = Microsoft
  TimeFormat = "epoch"
  Fields = [
        """\sact=({action}.+?)\s*\w+=""",
# addr is removed
        """\sapp=({app}.+?)\s*\w+=""",
        """\scn1=({cn1}.+?)\s*\w+=""",
        """\scn2=({cn2}.+?)\s*\w+=""",
        """\scn3=({cn3}.+?)\s*\w+=""",
# cnt is removed
        """\scs1=({cs1}.+?)\s*\w+=""",
        """\scs2=(None|({cs2}.+?))\s*\w+=""",
        """\scs3=({cs3}.+?)\s*\w+=""",
        """\scs4=({cs4}.+?)\s*\w+=""",
        """\scs5=({cs5}.+?)\s*\w+=""",
        """\scs6=\s*({cs6}.+?)\s*\w+=""",
        """\sdeviceDirection=({direction}.+?)\s*\w+=""",
        """\sdeviceFacility=({device_facility}.+?)\s*\w+=""",
        """\sdeviceInboundInterface=({src_interface}.+?)\s*\w+=""",
        """\sdeviceOutboundInterface=({dest_interface}.+?)\s*\w+=""",
        """\sdevicePayloadId=({device_id}.+?)\s*\w+=""",
        """\sdeviceProcessName =({process_name}.+?)\s*\w+=""",
        """\sdeviceSeverity=\\*(Unknown|({alert_severity}.+?))\s*\w+=""",
        """\sdestinationDnsDomain=({dest_domain}.+?)\s*\w+=""",
        """\sdestinationServiceName =({service_name}.+?)\s*\w+=""",
        """\sdestinationTranslatedAddress=({dest_translated_ip}[A-Fa-f:\d.]+)""",
        """\sdestinationTranslatedPort=({dest_translated_port}\d+)""",
        """\sfilePath=({file_path}.+?)\s*\w+=""",
        """\ssourceTranslatedAddress=({src_translated_ip}[A-Fa-f:\d.]+)""",
        """\ssourceTranslatedPort=({src_translated_port}\d+)""",
        """\sdhost=({dest_host}[\w\-.]+?)\s*\w+=""",
        """\sdproc=({dproc}.+?)\s*\w+=""",
        """\sdpt=({dest_port}\d+)""",
        """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s*\w+=""",
        """\sdtz=({dtz}.+?)\s*\w+=""",
        """\sduser=(N\/A|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\w+=""",
        """\sdvc=({host}[A-Fa-f:\d.]+)""",
        """\sdvchost=({host}[\w\-.]+)""",
# dvcp_id is removed
        """\serror='({result}[^']+)'""",
        """\seventId=({event_code}.+?)\s*\w+=""",
        """\sexternalId=({event_code}.+?)\s*\w+=""",
        """\sfileType=({file_type}.+?)\s*\w+=""",
        """\sflexString2=({flex_string2}.+?)\s*\w+=""",
        """\sfname=({file_name}.+?)\s*\w+=""",
        """\sgroup=({group_name}.+?)\s*\w+=""",
        """\sin=({bytes_in}\d+)""",
# msg is removed
        """\sout=({bytes_out}\d+)""",
        """\sproto=({protocol}.+?)\s*\w+=""",
        """\sreason=({result_reason}.+?)\s*\w+=""",
        """\srequest=({request}.+?)\s*\w+=""",
        """\srt=({time}\d{13})\s*\w+=""",
        """\sshost=({src_host}.+?)\s*\w+=""",
        """\ssourceDnsDomain=({src_domain}.+?)\s*\w+=""",
        """\sspid=({process_id}.+?)\s*\w+=""",
        """\sspt=({src_port}\d+)""",
# src is removed
        """\ssuid=(N\/A|-|({user_uid}.+?))\s*\w+=""",
        """\ssuser=(N\/A|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\w+=""",
        """\stime_reopen='({time}[^']+)'""",
        """\stype=({event_category}.+?)\s*\w+="""
        """CEF[^|]+\|({device_vendor}[^|]+)""",
# device_product is removed
        """CEF[^|]+\|([^|]*\|){2}({device_version}[^|]+)""",
        """CEF[^|]+\|([^|]*\|){3}({class_id}[^|]+)""",
        """CEF[^|]+\|([^|]*\|){4}({event_name}.+?)\s*\|(Unknown|({alert_severity}[^|]+?))\|\s*(\w+=|$)""",
  
}
```
#### Parser Content
```Java
{
Name = microfocusarcsight-ma-cef-app-activity-success-4363448
  Vendor = MicroFocus ArcSight
  Product = MicroFocus ArcSight
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """eventId=""" ]
  Fields = [
        """\sact=({act}.+?)\s*\w+=""",
        """\saddr='({addr}[^']+)',""",
        """\sapp=({app}.+?)\s*\w+=""",
        """\scn1=({cn1}.+?)\s*\w+=""",
        """\scn2=({cn2}.+?)\s*\w+=""",
        """\scn3=({cn3}.+?)\s*\w+=""",
        """\scnt=({cnt}.+?)\s*\w+=""",
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
        """\sfilePath=({filePath}.+?)\s*\w+=""",
        """\ssourceTranslatedAddress=({src_translated_ip}[A-Fa-f:\d.]+)""",
        """\ssourceTranslatedPort=({src_translated_port}\d+)""",
        """\sdhost=({dest_host}.+?)\s*\w+=""",
        """\sdproc=({dproc}.+?)\s*\w+=""",
        """\sdpt=({dest_port}\d+)""",
        """\sdst=({dest_ip}.+?)\s*\w+=""",
        """\sdtz=({dtz}.+?)\s*\w+=""",
        """\sduser=(N\/A|-|({user}[^\\\/\s]+?))\s*\w+=""",
        """\sdvc=({host}[A-Fa-f:\d.]+)""",
        """\sdvchost=({host}[\w\-.]+)""",
        """\sdvcpid=({dvcp_id}.+?)\s*\w+=""",
        """\serror='({result}[^']+)'""",
        """\seventId=({event_code}.+?)\s*\w+=""",
        """\sexternalId=({event_code}.+?)\s*\w+=""",
        """\sfileType=({file_type}.+?)\s*\w+=""",
        """\sflexString2=({flex_string2}.+?)\s*\w+=""",
        """\sfname=({file_name}.+?)\s*\w+=""",
        """\sgroup=({group_name}.+?)\s*\w+=""",
        """\sin=({bytes_in}\d+)""",
        """\smsg=({msg}.+?)\s*\w+=""",
        """\sout=({bytes_out}\d+)""",
        """\sproto=({protocol}.+?)\s*\w+=""",
        """\sreason=({reason}.+?)\s*\w+=""",
        """\srequest=({request}.+?)\s*\w+=""",
        """\srt=({time}.+?)\s*\w+=""",
        """\sshost=({src_host}.+?)\s*\w+=""",
        """\ssourceDnsDomain=({src_domain}.+?)\s*\w+=""",
        """\sspid=({spid}.+?)\s*\w+=""",
        """\sspt=({src_port}\d+)""",
        """\ssrc=({src}.+?)\s*\w+=""",
        """\ssuid=(N\/A|-|({suid}.+?))\s*\w+=""",
        """\ssuser=(N\/A|-|({user}.+?))\s*\w+=""",
        """\stime_reopen='({time}[^']+)'""",
        """\stype=({event_category}.+?)\s*\w+="""
        """CEF[^|]+\|({device_vendor}[^|]+)""",
        """CEF[^|]+\|([^|]*\|)({device_product}[^|]+)""",
        """CEF[^|]+\|([^|]*\|){2}({device_version}[^|]+)""",
        """CEF[^|]+\|([^|]*\|){3}({class_id}[^|]+)""",
        """CEF[^|]+\|([^|]*\|){4}({event_name}.+?)\s*\|(Unknown|({alert_severity}[^|]+?))\|\s*(\w+=|$)""",
  ]
  ParserVersion = "v1.0.0"


}
```
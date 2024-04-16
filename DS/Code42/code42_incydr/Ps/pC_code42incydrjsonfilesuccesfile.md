#### Parser Content
```Java
{
Name = code42-incydr-json-file-succes-file
  Vendor = Code42
  Product = Code42 Incydr
  ExtractionType = json
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions= [ """"action":""", """"file":{""", """Code42""",""""source":{""",""""destination":{""" ]
  Fields = [
    """exa_json_path=$.raw-event.@timestamp,exa_field_name=time""",
    """exa_json_path=$.raw-event.event.action,exa_field_name=event_name""",
    """exa_json_path=$.raw-event.user.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""",
    """exa_json_path=$.raw-event.file,exa_regex=\{"name":"({file_name}[^"]+?(\.({file_ext}[^"\.]+))?)"""",
    """exa_json_path=$.raw-event.file.directory,exa_field_name=file_dir""",
    """exa_json_path=$.raw-event.file.originalDirectory,exa_field_name=src_file_dir"""
    """exa_json_path=$.raw-event.file.category,exa_field_name=file_type""",
    """exa_json_path=$.raw-event.file,exa_regex="originalName":"({src_file_name}[^"\.]+(\.({src_file_ext}[^"]+))?)"""",
    """exa_json_path=$.raw-event.file,exa_regex="sizeInBytes":(({bytes}\d+))""",
    """exa_json_path=$.raw-event.source.name,exa_field_name=src_host""",
    """exa_json_path=$.raw-event.source.ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.raw-event.source.domain,exa_field_name=domain""",
    """exa_json_path=$.raw-event.source.removableMedia.busType,exa_field_name=device_type""",
    """exa_json_path=$.raw-event.source.removableMedia.mediaName,exa_field_name=device_name""",
    """exa_json_path=$.raw-event.source.removableMedia.serialNumber,exa_field_name=removable_media_serial_number""",
    """exa_json_path=$.raw-event.file.changeType,exa_field_name=operation,exa_match_expr=!InList(toLower($.raw-event.file.changeType),"none")""",
    """exa_json_path=$.raw-event.file.hash.md5,exa_field_name=hash_md5""",
    """exa_json_path=$.raw-event.file.hash.sha256,exa_field_name=hash_sha256""",
    """exa_json_path=$.raw-event.git.repositoryUri,exa_field_name=repository_name""",
    """exa_json_path=$.raw-event.destination.printerName,exa_field_name=printer_name"""
    """exa_json_path=$.raw-event.destination.printJobName,exa_field_name=object"""
    """exa_json_path=$.raw-event.risk.severity,exa_field_name=alert_severity""",
    """exa_json_path=$.raw-event.source.operatingSystem,exa_field_name=os""",
    """exa_json_path=$.raw-event.file.category,exa_field_name=file_category""",
    """exa_json_path=$.raw-event.file.mimeTypeByBytes,exa_field_name=mime""",
    """exa_json_path=$.raw-event.file,exa_regex="owner":"([^\\]+\\+)?({file_owner}[^"]+)"""",
    """exa_json_path=$.raw-event.file.url,exa_field_name=file_url""",
    """exa_json_path=$.raw-event.process.executable,exa_field_name=process_path""",
    """exa_json_path=$.raw-event.destination.user.email,exa_regex=({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""",
    """exa_json_path=$.raw-event.destination.category,exa_field_name=dest_group""",
  ]


}
```
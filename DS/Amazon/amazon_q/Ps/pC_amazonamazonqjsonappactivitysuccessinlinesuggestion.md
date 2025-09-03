#### Parser Content
```Java
{
Name = amazon-amazonq-json-app-activity-success-inlinesuggestion
  Vendor = "Amazon"
  Product = "Amazon Q"
  ExtractionType = json
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """"leftContext":""", """"rightContext":""", """"customizationArn":""", """"completions":""",  ]
  Fields = [
    """exa_json_path=$.records[0].generateCompletionsEventRequest.timeStamp,exa_field_name=time""",
    """exa_json_path=$.records[0].generateCompletionsEventRequest.fileName,exa_regex=({file_path}({file_dir}[^"]+[\/]+)?({file_name}[^"\\\/\.]+(.({file_ext}\w+))?))""",
    """exa_json_path=$.records[0].generateCompletionsEventRequest.userId,exa_field_name=user_id""",
    """exa_json_path=$.records[0].generateCompletionsEventResponse.requestId,exa_field_name=additional_info""",
   ]


}
```
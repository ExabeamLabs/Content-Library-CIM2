#### Parser Content
```Java
{
Name = "sentinelone-singularityp-json-alert-trigger-success-datasourcecategorysecurity-2"
  ExtractionType = json
  Conditions = [ """"dataSource.category":"security"""", """vendor_name":"SentinelOne"""", """"category_name":"Discovery"""" ]
  ParserVersion = "v1.0.0"

json-sentinelone-activitytype.Fields}[
    """exa_json_path=$.primaryDescription,exa_field_name=alert_name""",
    """exa_json_path=$..threatClassification,exa_field_name=alert_type""",
  ]
  ParserVersion = "v1.0.0"
},

${SentinelOneParsersTemplates.json-sentinelone-activitytype}{
  Name = sentinelone-singularityp-json-app-activity-success-activitytype4008
  Conditions = [ """"activityType":4008""", """"fileDisplayName":"""", """"primaryDescription":"""" ]
  Fields = ${SentinelOneParsersTemplates.json-sentinelone-activitytype.Fields}[
    """exa_json_path=$.primaryDescription,exa_field_name=operation""",
    """exa_json_path=$..threatClassification,exa_field_name=operation_type""",
  ]
  ParserVersion = "v1.0.0"
},
${SentinelOneParsersTemplates.json-sentinelone-activitytype}{
  Name = sentinelone-singularityp-json-app-activity-success-activitytype2004
  Conditions = [ """"activityType":2004""", """"fileDisplayName":"""", """"primaryDescription":"""" ]
  Fields = ${SentinelOneParsersTemplates.json-sentinelone-activitytype.Fields}[
    """exa_json_path=$.primaryDescription,exa_field_name=operation""",
    """exa_json_path=$..threatClassification,exa_field_name=operation_type""",
  ]
  ParserVersion = "v1.0.0"
},
${SentinelOneParsersTemplates.json-sentinelone-activitytype}{
  Name = sentinelone-singularityp-json-app-activity-success-activitytype2001
  Conditions = [ """"activityType":2001""", """"fileDisplayName":"""", """"primaryDescription":"""" ]
  Fields = ${SentinelOneParsersTemplates.json-sentinelone-activitytype.Fields}[
    """exa_json_path=$.primaryDescription,exa_field_name=operation""",
    """exa_json_path=$..threatClassification,exa_field_name=operation_type""",
  ]
  ParserVersion = "v1.0.0"
},

${SentinelOneParsersTemplates.json-sentinelone-activitytype}{
  Name = sentinelone-singularityp-json-app-login-fail-133
  ParserVersion = v1.0.0
  Conditions = [ """"primaryDescription":""", """"activityType":133,""", """"activityUuid":""", """"threatId":""" ]
  Fields = ${SentinelOneParsersTemplates.json-sentinelone-activitytype.Fields} [
    """exa_json_path=$..reason,exa_field_name=failure_reason"""  
}
```
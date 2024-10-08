#### Parser Content
```Java
{
Name = "netskope-sc-cef-file-read-success-preview"
  Conditions = [
""""type":""""
""""ccl":"""
""""activity":"Preview""""
""""object_type":"File""""
  ]
  ParserVersion = "v1.0.0"

cef-netskope-activity.DupFields}[
"operation->access"
  ]
  Name = "netskope-sc-cef-file-upload-success-upload"
  Conditions = [
""""type":""""
"""destinationServiceName =Netskope"""
""""activity":"Upload""""
""""object_type":"File""""
  ]
  ParserVersion = "v1.0.0"
},

${NetskopeParsersTemplates.cef-netskope-activity}{
  DupFields = ${NetskopeParsersTemplates.cef-netskope-activity.DupFields}[
"operation->access"
  ]
  Name = "netskope-sc-cef-file-read-success-view"
  Conditions = [
""""type":""""
""""ccl":"""
""""activity":"View""""
""""object_type":"File""""
  ]
  ParserVersion = "v1.0.0"
},

${NetskopeParsersTemplates.cef-netskope-activity}{
  DupFields = ${NetskopeParsersTemplates.cef-netskope-activity.DupFields}[
"operation->access"
  ]
  Name = "netskope-sc-cef-file-read-success-viewall"
  Conditions = [
""""type":""""
""""ccl":"""
""""activity":"View All""""
""""object_type":"File""""
  ]
  ParserVersion = "v1.0.0"
},

${NetskopeParsersTemplates.cef-netskope-activity}{
  DupFields = ${NetskopeParsersTemplates.cef-netskope-activity.DupFields}[
"operation->access"
  ]
  Name = "netskope-sc-cef-file-read-success-accessedextended"
  Conditions = [
""""type":""""
""""ccl":"""
""""activity":"FileAccessedExtended""""
  ]
  ParserVersion = "v1.0.0"
},

${NetskopeParsersTemplates.cef-netskope-activity}{
  DupFields = ${NetskopeParsersTemplates.cef-netskope-activity.DupFields}[
"operation->access"
  ]
  Name = "netskope-sc-cef-file-write-success-modifiedextended"
  Conditions = [
""""type":""""
""""ccl":"""
""""activity":"FileModifiedExtended""""
  ]
  ParserVersion = "v1.0.0"
},

${NetskopeParsersTemplates.cef-netskope-activity}{
  DupFields = ${NetskopeParsersTemplates.cef-netskope-activity.DupFields}[
"operation->access"
  ]
  Name = "netskope-sc-cef-file-write-success-listupdated"
  Conditions = [
""""type":""""
""""ccl":"""
""""activity":"ListUpdated""""
  ]
  ParserVersion = "v1.0.0"
},

${NetskopeParsersTemplates.cef-netskope-activity}{
  DupFields = ${NetskopeParsersTemplates.cef-netskope-activity.DupFields}[
"operation->access"
  ]
  Name = "netskope-sc-cef-file-write-success-listcolumncreated"
  Conditions = [
""""type":""""
""""ccl":"""
""""activity":"ListColumnCreated""""
  ]
  ParserVersion = "v1.0.0"
},

${NetskopeParsersTemplates.cef-netskope-activity}{
  DupFields = ${NetskopeParsersTemplates.cef-netskope-activity.DupFields}[
"operation->access"
  ]
  Name = "netskope-sc-cef-file-write-success-listcreated"
  Conditions = [
""""type":""""
""""ccl":"""
""""activity":"ListCreated""""
  ]
  ParserVersion = "v1.0.0"
},

${NetskopeParsersTemplates.cef-netskope-activity}{
  DupFields = ${NetskopeParsersTemplates.cef-netskope-activity.DupFields}[
"operation->access"
  ]
  Name = "netskope-sc-cef-file-delete-success-listitemdeleted"
  Conditions = [
""""type":""""
""""ccl":"""
""""activity":"ListItemDeleted""""
  ]
  ParserVersion = "v1.0.0"
},

${NetskopeParsersTemplates.cef-netskope-activity}{
  DupFields = ${NetskopeParsersTemplates.cef-netskope-activity.DupFields}[
"operation->access"
  ]
  Name = "netskope-sc-cef-file-write-success-listitemupdated"
  Conditions = [
""""type":""""
""""ccl":"""
""""activity":"ListItemUpdated""""
  ]
  ParserVersion = "v1.0.0"
},

${NetskopeParsersTemplates.cef-netskope-activity}{
  DupFields = ${NetskopeParsersTemplates.cef-netskope-activity.DupFields}[
"operation->access"
  ]
  Name = "netskope-sc-cef-file-delete-success-filedeleted"
  Conditions = [
""""type":""""
""""ccl":"""
""""activity":"FileDeleted"""
  ]
  ParserVersion = "v1.0.0"
},

${NetskopeParsersTemplates.cef-netskope-activity}{
  DupFields = ${NetskopeParsersTemplates.cef-netskope-activity.DupFields}[
"operation->access"
  ]
  Name = "netskope-sc-cef-file-read-success-pageviewedextended"
  Conditions = [
""""type":""""
""""ccl":"""
""""activity":"PageViewedExtended""""
  ]
  ParserVersion = "v1.0.0"
},

${NetskopeParsersTemplates.cef-netskope-activity}{
  DupFields = ${NetskopeParsersTemplates.cef-netskope-activity.DupFields}[
"operation->access"
  ]
  Name = "netskope-sc-cef-file-write-success-create"
  Conditions = [
""""type":""""
""""ccl":"""
""""activity":"Create""""
""""object_type":"File""""
  ]
  ParserVersion = "v1.0.0"
},

${NetskopeParsersTemplates.cef-netskope-activity}{
  DupFields = ${NetskopeParsersTemplates.cef-netskope-activity.DupFields}[
"operation->access"
  ]
  Name = "netskope-sc-cef-file-delete-success-delete"
  Conditions = [
""""type":""""
""""ccl":"""
""""activity":"Delete""""
""""object_type":"File""""
  ]
  ParserVersion = "v1.0.0"
},

${NetskopeParsersTemplates.cef-netskope-activity}{
  DupFields = ${NetskopeParsersTemplates.cef-netskope-activity.DupFields}[
"operation->access"
  ]
  Name = "netskope-sc-cef-file-download-success-download"
  Conditions = [
""""type":""""
"""destinationServiceName =Netskope"""
""""activity":"Download""""
""""object_type":"File""""
  ]
  ParserVersion = "v1.0.0"
},

${NetskopeParsersTemplates.cef-netskope-activity}{
  DupFields = ${NetskopeParsersTemplates.cef-netskope-activity.DupFields}[
"operation->access"
  ]
  Name = "netskope-sc-cef-file-write-success-edit"
  Conditions = [
""""type":""""
""""ccl":"""
""""activity":"Edit""""
""""object_type":"File""""
  ]
  ParserVersion = "v1.0.0"
},

${NetskopeParsersTemplates.cef-netskope-activity}{
  DupFields = ${NetskopeParsersTemplates.cef-netskope-activity.DupFields}[
"operation->access"
  ]
  Name = "netskope-sc-cef-file-write-success-move"
  Conditions = [
""""type":""""
""""ccl":"""
""""activity":"Move""""
""""object_type":"File""""
  ]
  ParserVersion = "v1.0.0"
},

${NetskopeParsersTemplates.cef-netskope-activity}{
  DupFields = ${NetskopeParsersTemplates.cef-netskope-activity.DupFields}[
"operation->access"
  ]
  Name = "netskope-sc-cef-file-permission-modify-success-share"
  Conditions = [
""""type":""""
""""ccl":"""
""""activity":"Share""""
""""object_type":"File""""
  ]
  ParserVersion = "v1.0.0"
},
${NetskopeParsersTemplates.cef-netskope-activity}{
  Name = netskope-sc-sk4-app-activity-success-follow
  ParserVersion = v1.0.0
  Conditions = [ """"type":"""", """"ccl":""", """"activity":"Follow"""" 
}
```
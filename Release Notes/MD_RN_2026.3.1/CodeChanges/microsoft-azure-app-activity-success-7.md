# Code Changes for microsoft-azure-app-activity-success-7 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'microsoft-azuremon-json-file-storagecategory') && !InList(toLower(operation), 'createfile', 'createshare', 'createtable', 'deletefile', 'deleteshare', 'deletetable', 'getdirectoryproperties', 'getfile', 'getfileproperties', 'getfileserviceproperties', 'getfileshareuniqueid', 'listfiles', 'putrange', 'querytables', 'setfileproperties', 'setsharemetadata', 'setshareproperties', 'snapshotshare', 'queryentities', 'insertentity', 'listblobs', 'listcontainers', 'getpageranges', 'listshares', 'listqueues','read','write','create','getfilepermission') |
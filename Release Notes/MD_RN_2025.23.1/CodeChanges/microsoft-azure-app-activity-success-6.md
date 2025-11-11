# Code Changes for microsoft-azure-app-activity-success-6 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'microsoft-azure-json-file-success-1', 'microsoft-azure-json-file-success-2') && containsAny(toLower(operation), 'properties', 'metadata', 'tag','bloblease','renewcontainerlease','acquirecontainerlease','batchrequest','blobpreflightrequest','getaccountinformation','getuserdelegationkey','getblocklist','getpathaccesscontrol','setblobtier','getwebcontent','outblockfromurl','putblobfromurl','publish') && !startsWithAny(result_code, '4') |
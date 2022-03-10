# \DefaultApi

All URIs are relative to *http://localhost:37740/etapi*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_note**](DefaultApi.md#create_note) | **POST** /create-note | 
[**delete_attribute_by_id**](DefaultApi.md#delete_attribute_by_id) | **DELETE** /attributes/{attributeId} | 
[**delete_branch_by_id**](DefaultApi.md#delete_branch_by_id) | **DELETE** /branches/{branchId} | 
[**delete_note_by_id**](DefaultApi.md#delete_note_by_id) | **DELETE** /notes/{noteId} | 
[**get_app_info**](DefaultApi.md#get_app_info) | **GET** /app-info | 
[**get_attribute_by_id**](DefaultApi.md#get_attribute_by_id) | **GET** /attributes/{attributeId} | 
[**get_branch_by_id**](DefaultApi.md#get_branch_by_id) | **GET** /branches/{branchId} | 
[**get_day_note**](DefaultApi.md#get_day_note) | **GET** /calendar/days/{date} | 
[**get_inbox_note**](DefaultApi.md#get_inbox_note) | **GET** /inbox/{date} | 
[**get_month_note**](DefaultApi.md#get_month_note) | **GET** /calendar/months/{month} | 
[**get_note_by_id**](DefaultApi.md#get_note_by_id) | **GET** /notes/{noteId} | 
[**get_week_note**](DefaultApi.md#get_week_note) | **GET** /calendar/weeks/{date} | 
[**get_year_note**](DefaultApi.md#get_year_note) | **GET** /calendar/years/{year} | 
[**login**](DefaultApi.md#login) | **POST** /auth/login | 
[**logout**](DefaultApi.md#logout) | **POST** /auth/logout | 
[**patch_attribute_by_id**](DefaultApi.md#patch_attribute_by_id) | **PATCH** /attributes/{attributeId} | 
[**patch_branch_by_id**](DefaultApi.md#patch_branch_by_id) | **PATCH** /branches/{branchId} | 
[**patch_note_by_id**](DefaultApi.md#patch_note_by_id) | **PATCH** /notes/{noteId} | 
[**post_attribute**](DefaultApi.md#post_attribute) | **POST** /attributes/{attributeId} | 
[**post_branch**](DefaultApi.md#post_branch) | **POST** /branches/{branchId} | 
[**post_refresh_note_ordering**](DefaultApi.md#post_refresh_note_ordering) | **POST** /refresh-note-ordering/{parentNoteId} | 
[**search_notes**](DefaultApi.md#search_notes) | **GET** /notes | 



## create_note

> serde_json::Value create_note(create_note_def)


Create a note and place it into the note tree

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_note_def** | [**CreateNoteDef**](CreateNoteDef.md) |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

[EtapiTokenAuth](../README.md#EtapiTokenAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_attribute_by_id

> delete_attribute_by_id(attribute_id)


deletes a attribute based on the attributeId supplied.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**attribute_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[EtapiTokenAuth](../README.md#EtapiTokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_branch_by_id

> delete_branch_by_id(branch_id)


deletes a branch based on the branchId supplied. If this is the last branch of the (child) note,  then the note is deleted as well. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**branch_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[EtapiTokenAuth](../README.md#EtapiTokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_note_by_id

> delete_note_by_id(note_id)


deletes a single note based on the noteId supplied

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**note_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[EtapiTokenAuth](../README.md#EtapiTokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_app_info

> crate::models::AppInfo get_app_info()


returns information about the running Trilium instance

### Parameters

This endpoint does not need any parameter.

### Return type

[**crate::models::AppInfo**](AppInfo.md)

### Authorization

[EtapiTokenAuth](../README.md#EtapiTokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_attribute_by_id

> crate::models::Attribute get_attribute_by_id(attribute_id)


Returns an attribute identified by its ID

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**attribute_id** | **String** |  | [required] |

### Return type

[**crate::models::Attribute**](Attribute.md)

### Authorization

[EtapiTokenAuth](../README.md#EtapiTokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_branch_by_id

> crate::models::Branch get_branch_by_id(branch_id)


Returns a branch identified by its ID

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**branch_id** | **String** |  | [required] |

### Return type

[**crate::models::Branch**](Branch.md)

### Authorization

[EtapiTokenAuth](../README.md#EtapiTokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_day_note

> crate::models::Note get_day_note(date)


returns a day note for a given date. Gets created if doesn't exist.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**date** | **String** |  | [required] |

### Return type

[**crate::models::Note**](Note.md)

### Authorization

[EtapiTokenAuth](../README.md#EtapiTokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_inbox_note

> crate::models::Note get_inbox_note(date)


returns an \"inbox\" note, into which note can be created. Date will be used depending on whether the inbox is a fixed note (identified with #inbox label) or a day note in a journal. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**date** | **String** |  | [required] |

### Return type

[**crate::models::Note**](Note.md)

### Authorization

[EtapiTokenAuth](../README.md#EtapiTokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_month_note

> crate::models::Note get_month_note(month)


returns a week note for a given date. Gets created if doesn't exist.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**month** | **String** |  | [required] |

### Return type

[**crate::models::Note**](Note.md)

### Authorization

[EtapiTokenAuth](../README.md#EtapiTokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_note_by_id

> crate::models::Note get_note_by_id(note_id)


Returns a note identified by its ID

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**note_id** | **String** |  | [required] |

### Return type

[**crate::models::Note**](Note.md)

### Authorization

[EtapiTokenAuth](../README.md#EtapiTokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_week_note

> crate::models::Note get_week_note(date)


returns a week note for a given date. Gets created if doesn't exist.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**date** | **String** |  | [required] |

### Return type

[**crate::models::Note**](Note.md)

### Authorization

[EtapiTokenAuth](../README.md#EtapiTokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_year_note

> crate::models::Note get_year_note(year)


returns a week note for a given date. Gets created if doesn't exist.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**year** | **String** |  | [required] |

### Return type

[**crate::models::Note**](Note.md)

### Authorization

[EtapiTokenAuth](../README.md#EtapiTokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## login

> serde_json::Value login(UNKNOWN_BASE_TYPE)


get an ETAPI token based on password for further use with ETAPI

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**UNKNOWN_BASE_TYPE** | Option<[**UNKNOWN_BASE_TYPE**](UNKNOWN_BASE_TYPE.md)> |  | [required] |

### Return type

[**serde_json::Value**](serde_json::Value.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## logout

> logout()


logout (delete/deactivate) an ETAPI token

### Parameters

This endpoint does not need any parameter.

### Return type

 (empty response body)

### Authorization

[EtapiTokenAuth](../README.md#EtapiTokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## patch_attribute_by_id

> crate::models::Attribute patch_attribute_by_id(attribute_id, attribute)


patch a attribute identified by the attributeId with changes in the body

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**attribute_id** | **String** |  | [required] |
**attribute** | [**Attribute**](Attribute.md) |  | [required] |

### Return type

[**crate::models::Attribute**](Attribute.md)

### Authorization

[EtapiTokenAuth](../README.md#EtapiTokenAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## patch_branch_by_id

> crate::models::Branch patch_branch_by_id(branch_id, branch)


patch a branch identified by the branchId with changes in the body

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**branch_id** | **String** |  | [required] |
**branch** | [**Branch**](Branch.md) |  | [required] |

### Return type

[**crate::models::Branch**](Branch.md)

### Authorization

[EtapiTokenAuth](../README.md#EtapiTokenAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## patch_note_by_id

> crate::models::Note patch_note_by_id(note_id, note)


patch a note identified by the noteId with changes in the body

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**note_id** | **String** |  | [required] |
**note** | [**Note**](Note.md) |  | [required] |

### Return type

[**crate::models::Note**](Note.md)

### Authorization

[EtapiTokenAuth](../README.md#EtapiTokenAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## post_attribute

> crate::models::Attribute post_attribute(attribute_id, attribute)


create an attribute for a given note

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**attribute_id** | **String** |  | [required] |
**attribute** | [**Attribute**](Attribute.md) |  | [required] |

### Return type

[**crate::models::Attribute**](Attribute.md)

### Authorization

[EtapiTokenAuth](../README.md#EtapiTokenAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## post_branch

> crate::models::Branch post_branch(branch_id, branch)


Create a branch (clone a note to a different location in the tree). In case there is a branch between parent note and child note already,  then this will update the existing branch with prefix, notePosition and isExpanded. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**branch_id** | **String** |  | [required] |
**branch** | [**Branch**](Branch.md) |  | [required] |

### Return type

[**crate::models::Branch**](Branch.md)

### Authorization

[EtapiTokenAuth](../README.md#EtapiTokenAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## post_refresh_note_ordering

> post_refresh_note_ordering(parent_note_id)


notePositions in branches are not automatically pushed to connected clients and need a specific instruction.  If you want your changes to be in effect immediately, call this service after setting branches' notePosition.  Note that you need to supply \"parentNoteId\" of branch(es) with changed positions. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**parent_note_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[EtapiTokenAuth](../README.md#EtapiTokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## search_notes

> crate::models::SearchResponse search_notes(search, fast_search, include_archived_notes, ancestor_note_id, ancestor_depth, order_by, order_direction, limit, debug)


Search notes

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**search** | **String** | search query string as described in https://github.com/zadam/trilium/wiki/Search | [required] |
**fast_search** | Option<**bool**> | enable fast search (fulltext doesn't look into content) |  |[default to false]
**include_archived_notes** | Option<**bool**> | search by default ignores archived notes. Set to 'true' to includes archived notes into search results. |  |[default to false]
**ancestor_note_id** | Option<**String**> | search only in a subtree identified by the subtree noteId. By default whole tree is searched. |  |
**ancestor_depth** | Option<**String**> | define how deep in the tree should the notes be searched |  |
**order_by** | Option<**String**> | name of the property/label to order search results by |  |
**order_direction** | Option<**String**> | order direction, ascending or descending |  |[default to asc]
**limit** | Option<**i32**> | limit the number of results you want to receive |  |
**debug** | Option<**bool**> | set to true to get debug information in the response (search query parsing) |  |[default to false]

### Return type

[**crate::models::SearchResponse**](SearchResponse.md)

### Authorization

[EtapiTokenAuth](../README.md#EtapiTokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


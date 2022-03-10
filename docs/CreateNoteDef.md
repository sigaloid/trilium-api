# CreateNoteDef

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**parent_note_id** | **String** |  | 
**title** | **String** |  | 
**_type** | **String** |  | 
**mime** | Option<**String**> | this needs to be specified only for note types 'code', 'file', 'image'. | [optional]
**content** | **String** |  | 
**note_position** | Option<**i32**> | Position of the note in the parent. Normal ordering is 10, 20, 30 ...  So if you want to create a note on the first position, use e.g. 5, for second position 15, for last e.g. 1000000  | [optional]
**prefix** | Option<**String**> | Prefix is branch (placement) specific title prefix for the note.  Let's say you have your note placed into two different places in the tree,  but you want to change the title a bit in one of the placements. For this you can use prefix.  | [optional]
**is_expanded** | Option<**bool**> | true if this note (as a folder) should appear expanded | [optional]
**note_id** | Option<**String**> |  | [optional]
**branch_id** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# \MenuApi

All URIs are relative to *http://localhost:8080/CFD/1.0.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddMenuItem**](MenuApi.md#AddMenuItem) | **Post** /menu | Create a menu item
[**ListMenu**](MenuApi.md#ListMenu) | **Get** /menu | List all menu items
[**ShowMenuItemById**](MenuApi.md#ShowMenuItemById) | **Get** /menu/{itemId} | Info for a specific menu item



## AddMenuItem

> AddMenuItem(ctx).MenuItem(menuItem).Execute()

Create a menu item



### Example

```go
package main

import (
    "context"
    "fmt"
    "os"
    openapiclient "./openapi"
)

func main() {
    menuItem := *openapiclient.NewMenuItem(int32(123), "Description_example", "Name_example", float32(123), int32(123)) // MenuItem | Item to add to the store

    configuration := openapiclient.NewConfiguration()
    apiClient := openapiclient.NewAPIClient(configuration)
    resp, r, err := apiClient.MenuApi.AddMenuItem(context.Background()).MenuItem(menuItem).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `MenuApi.AddMenuItem``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
    }
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddMenuItemRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **menuItem** | [**MenuItem**](MenuItem.md) | Item to add to the store | 

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListMenu

> []MenuItem ListMenu(ctx).Limit(limit).Execute()

List all menu items

### Example

```go
package main

import (
    "context"
    "fmt"
    "os"
    openapiclient "./openapi"
)

func main() {
    limit := int32(56) // int32 | How many items to return at one time (max 100) (optional)

    configuration := openapiclient.NewConfiguration()
    apiClient := openapiclient.NewAPIClient(configuration)
    resp, r, err := apiClient.MenuApi.ListMenu(context.Background()).Limit(limit).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `MenuApi.ListMenu``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
    }
    // response from `ListMenu`: []MenuItem
    fmt.Fprintf(os.Stdout, "Response from `MenuApi.ListMenu`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListMenuRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int32** | How many items to return at one time (max 100) | 

### Return type

[**[]MenuItem**](MenuItem.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ShowMenuItemById

> MenuItem ShowMenuItemById(ctx, itemId).Execute()

Info for a specific menu item

### Example

```go
package main

import (
    "context"
    "fmt"
    "os"
    openapiclient "./openapi"
)

func main() {
    itemId := "itemId_example" // string | The id of the menu item to retrieve

    configuration := openapiclient.NewConfiguration()
    apiClient := openapiclient.NewAPIClient(configuration)
    resp, r, err := apiClient.MenuApi.ShowMenuItemById(context.Background(), itemId).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `MenuApi.ShowMenuItemById``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
    }
    // response from `ShowMenuItemById`: MenuItem
    fmt.Fprintf(os.Stdout, "Response from `MenuApi.ShowMenuItemById`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**itemId** | **string** | The id of the menu item to retrieve | 

### Other Parameters

Other parameters are passed through a pointer to a apiShowMenuItemByIdRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**MenuItem**](MenuItem.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


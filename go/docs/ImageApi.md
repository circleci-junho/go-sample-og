# \ImageApi

All URIs are relative to *http://localhost:8080/CFD/1.0.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddImage**](ImageApi.md#AddImage) | **Post** /image | Add an image to the restaraunt
[**DeleteImage**](ImageApi.md#DeleteImage) | **Delete** /image/{imageId} | Remove image
[**GetImage**](ImageApi.md#GetImage) | **Get** /image/{imageId} | Get image



## AddImage

> AddImage200Response AddImage(ctx).FileName(fileName).Execute()

Add an image to the restaraunt



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
    fileName := os.NewFile(1234, "some_file") // *os.File |  (optional)

    configuration := openapiclient.NewConfiguration()
    apiClient := openapiclient.NewAPIClient(configuration)
    resp, r, err := apiClient.ImageApi.AddImage(context.Background()).FileName(fileName).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `ImageApi.AddImage``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
    }
    // response from `AddImage`: AddImage200Response
    fmt.Fprintf(os.Stdout, "Response from `ImageApi.AddImage`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiAddImageRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fileName** | ***os.File** |  | 

### Return type

[**AddImage200Response**](AddImage200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteImage

> DeleteImage(ctx, imageId).Execute()

Remove image



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
    imageId := int32(56) // int32 | The imageId to delete

    configuration := openapiclient.NewConfiguration()
    apiClient := openapiclient.NewAPIClient(configuration)
    resp, r, err := apiClient.ImageApi.DeleteImage(context.Background(), imageId).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `ImageApi.DeleteImage``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
    }
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**imageId** | **int32** | The imageId to delete | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteImageRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetImage

> *os.File GetImage(ctx, imageId).Execute()

Get image



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
    imageId := int32(56) // int32 | The imageId of the image to retrieve

    configuration := openapiclient.NewConfiguration()
    apiClient := openapiclient.NewAPIClient(configuration)
    resp, r, err := apiClient.ImageApi.GetImage(context.Background(), imageId).Execute()
    if err != nil {
        fmt.Fprintf(os.Stderr, "Error when calling `ImageApi.GetImage``: %v\n", err)
        fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
    }
    // response from `GetImage`: *os.File
    fmt.Fprintf(os.Stdout, "Response from `ImageApi.GetImage`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**imageId** | **int32** | The imageId of the image to retrieve | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetImageRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[***os.File**](*os.File.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: image/png

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


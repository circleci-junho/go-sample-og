# MenuItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **int32** |  | 
**Description** | **string** |  | 
**Name** | **string** |  | 
**Price** | **float32** |  | 
**ImageId** | **int32** | URL to an image of the menu item. This should be the image from the /image endpoint  | 

## Methods

### NewMenuItem

`func NewMenuItem(id int32, description string, name string, price float32, imageId int32, ) *MenuItem`

NewMenuItem instantiates a new MenuItem object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewMenuItemWithDefaults

`func NewMenuItemWithDefaults() *MenuItem`

NewMenuItemWithDefaults instantiates a new MenuItem object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *MenuItem) GetId() int32`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *MenuItem) GetIdOk() (*int32, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *MenuItem) SetId(v int32)`

SetId sets Id field to given value.


### GetDescription

`func (o *MenuItem) GetDescription() string`

GetDescription returns the Description field if non-nil, zero value otherwise.

### GetDescriptionOk

`func (o *MenuItem) GetDescriptionOk() (*string, bool)`

GetDescriptionOk returns a tuple with the Description field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDescription

`func (o *MenuItem) SetDescription(v string)`

SetDescription sets Description field to given value.


### GetName

`func (o *MenuItem) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *MenuItem) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *MenuItem) SetName(v string)`

SetName sets Name field to given value.


### GetPrice

`func (o *MenuItem) GetPrice() float32`

GetPrice returns the Price field if non-nil, zero value otherwise.

### GetPriceOk

`func (o *MenuItem) GetPriceOk() (*float32, bool)`

GetPriceOk returns a tuple with the Price field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPrice

`func (o *MenuItem) SetPrice(v float32)`

SetPrice sets Price field to given value.


### GetImageId

`func (o *MenuItem) GetImageId() int32`

GetImageId returns the ImageId field if non-nil, zero value otherwise.

### GetImageIdOk

`func (o *MenuItem) GetImageIdOk() (*int32, bool)`

GetImageIdOk returns a tuple with the ImageId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetImageId

`func (o *MenuItem) SetImageId(v int32)`

SetImageId sets ImageId field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



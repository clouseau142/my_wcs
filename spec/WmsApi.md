# WmsApi

All URIs are relative to *https://virtserver.swaggerhub.com/MyWHOrg/picking_in_go/1.0.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addOrder**](WmsApi.md#addOrder) | **POST** /order | adds an order to the system
[**addPickrequestToOrder**](WmsApi.md#addPickrequestToOrder) | **POST** /order/{orderId}/pickrequest | adds a pick to an order
[**searchOrders**](WmsApi.md#searchOrders) | **GET** /orders | searches orders the system
[**searchPickRequests**](WmsApi.md#searchPickRequests) | **GET** /order/{orderId}/pickrequests | searches all pickrequests within an order and returns the pickrequests
[**searchSingleOrder**](WmsApi.md#searchSingleOrder) | **GET** /order/{orderId} | searches one specific order
[**searchSinglePickRequest**](WmsApi.md#searchSinglePickRequest) | **GET** /order/{orderId}/pickrequest/{pickId} | searches one specific pickrequest within an order and returns the pickrequest

<a name="addOrder"></a>
# **addOrder**
> addOrder(body)

adds an order to the system

adds an order

### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.WmsApi;


WmsApi apiInstance = new WmsApi();
Order body = new Order(); // Order | order to be added to batch
try {
    apiInstance.addOrder(body);
} catch (ApiException e) {
    System.err.println("Exception when calling WmsApi#addOrder");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Order**](Order.md)| order to be added to batch | [optional]

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

<a name="addPickrequestToOrder"></a>
# **addPickrequestToOrder**
> addPickrequestToOrder(orderId, body)

adds a pick to an order

adds a pickrequest to an order

### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.WmsApi;


WmsApi apiInstance = new WmsApi();
OrderpropertiesorderId orderId = new OrderpropertiesorderId(); // OrderpropertiesorderId | 
Pickrequests body = new Pickrequests(); // Pickrequests | pick to be added to an order
try {
    apiInstance.addPickrequestToOrder(orderId, body);
} catch (ApiException e) {
    System.err.println("Exception when calling WmsApi#addPickrequestToOrder");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderId** | [**OrderpropertiesorderId**](.md)|  |
 **body** | [**Pickrequests**](Pickrequests.md)| pick to be added to an order | [optional]

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

<a name="searchOrders"></a>
# **searchOrders**
> List&lt;Order&gt; searchOrders(searchString, skip, limit)

searches orders the system

By passing in the appropriate options, you can search for certain batches in the system

### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.WmsApi;


WmsApi apiInstance = new WmsApi();
String searchString = "searchString_example"; // String | pass an optional search string for looking up orders
Integer skip = 56; // Integer | number of records to skip for pagination
Integer limit = 56; // Integer | maximum number of records to return
try {
    List<Order> result = apiInstance.searchOrders(searchString, skip, limit);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WmsApi#searchOrders");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **searchString** | **String**| pass an optional search string for looking up orders | [optional]
 **skip** | **Integer**| number of records to skip for pagination | [optional] [enum: ]
 **limit** | **Integer**| maximum number of records to return | [optional] [enum: ]

### Return type

[**List&lt;Order&gt;**](Order.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="searchPickRequests"></a>
# **searchPickRequests**
> Pickrequest searchPickRequests(orderId)

searches all pickrequests within an order and returns the pickrequests

By passing in the appropriate options, you can search in the system

### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.WmsApi;


WmsApi apiInstance = new WmsApi();
List<OrderpropertiesorderId> orderId = Arrays.asList(new OrderpropertiesorderId()); // List<OrderpropertiesorderId> | 
try {
    Pickrequest result = apiInstance.searchPickRequests(orderId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WmsApi#searchPickRequests");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderId** | [**List&lt;OrderpropertiesorderId&gt;**](OrderpropertiesorderId.md)|  |

### Return type

[**Pickrequest**](Pickrequest.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="searchSingleOrder"></a>
# **searchSingleOrder**
> CompleteOrder searchSingleOrder(orderId)

searches one specific order

By passing in the appropriate options, you can search for certain batches in the system

### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.WmsApi;


WmsApi apiInstance = new WmsApi();
List<OrderpropertiesorderId> orderId = Arrays.asList(new OrderpropertiesorderId()); // List<OrderpropertiesorderId> | 
try {
    CompleteOrder result = apiInstance.searchSingleOrder(orderId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WmsApi#searchSingleOrder");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderId** | [**List&lt;OrderpropertiesorderId&gt;**](OrderpropertiesorderId.md)|  |

### Return type

[**CompleteOrder**](CompleteOrder.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="searchSinglePickRequest"></a>
# **searchSinglePickRequest**
> Pickrequest searchSinglePickRequest(orderId, pickId)

searches one specific pickrequest within an order and returns the pickrequest

By passing in the appropriate options, you can search in the system

### Example
```java
// Import classes:
//import io.swagger.client.ApiException;
//import io.swagger.client.api.WmsApi;


WmsApi apiInstance = new WmsApi();
List<OrderpropertiesorderId> orderId = Arrays.asList(new OrderpropertiesorderId()); // List<OrderpropertiesorderId> | 
List<PickrequestpropertiespickrequestId> pickId = Arrays.asList(new PickrequestpropertiespickrequestId()); // List<PickrequestpropertiespickrequestId> | 
try {
    Pickrequest result = apiInstance.searchSinglePickRequest(orderId, pickId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WmsApi#searchSinglePickRequest");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderId** | [**List&lt;OrderpropertiesorderId&gt;**](OrderpropertiesorderId.md)|  |
 **pickId** | [**List&lt;PickrequestpropertiespickrequestId&gt;**](PickrequestpropertiespickrequestId.md)|  |

### Return type

[**Pickrequest**](Pickrequest.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


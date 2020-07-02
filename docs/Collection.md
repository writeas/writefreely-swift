# Collection

``` swift
public struct Collection
```

## Inheritance

`Decodable`

## Initializers

### `init(title:alias:)`

Creates a basic `Collection` object.

``` swift
public init(title: String, alias: String?)
```

This initializer creates a bare-minimum `Collection` object for sending to the server; use the decoder-based
initializer to populate its other properties from the server response.

If no `alias` parameter is provided, one will be generated by the server.

#### Parameters

  - title: - title: The title to give the Collection.
  - alias: - alias: The alias for the Collection.

### `init(from:)`

Creates a `Collection` object from the server response.

``` swift
public init(from decoder: Decoder) throws
```

Primarily used by the `WriteFreelyClient` to create a `Collection` object from the JSON returned by the server.

#### Parameters

  - decoder: - decoder: The decoder to use for translating the server response to a Swift object.

#### Throws

Error thrown by the `try` attempt when decoding any given property.

## Properties

### `alias`

``` swift
var alias: String?
```

### `title`

``` swift
var title: String
```

### `description`

``` swift
var description: String?
```

### `styleSheet`

``` swift
var styleSheet: String?
```

### `isPublic`

``` swift
var isPublic: Bool?
```

### `views`

``` swift
var views: Int?
```

### `email`

``` swift
var email: String?
```

### `url`

``` swift
var url: String?
```
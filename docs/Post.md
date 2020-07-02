# Post

``` swift
public struct Post
```

## Inheritance

`Decodable`

## Initializers

### `init(body:title:appearance:language:rtl:createdDate:)`

Creates a basic `Post` object.

``` swift
public init(body: String, title: String? = nil, appearance: String? = nil, language: String? = nil, rtl: Bool? = nil, createdDate: Date? = nil)
```

This initializer creates a bare-minimum `Post` object for sending to the server; use the decoder-based
initializer to populate its other properties from the server response.

Only the `body` parameter is required. If other properties are not provided, they will be generated by
the server.

#### Parameters

  - body: - body: The body text for the post.
  - title: - title: The title for the post.
  - appearance: - appearance: The appearance for the post; one of `sans`, `serif`/`norm`, `wrap`, `mono`,  or `code`. Defaults to `serif`.
  - language: - language: An ISO 639-1 language code.
  - rtl: - rtl: Set to `true` to show content right-to-left.
  - createdDate: - createdDate: The published date for the post.

### `init(from:)`

Creates a `Post` object from the server response.

``` swift
public init(from decoder: Decoder) throws
```

Primarily used by the `WriteFreelyClient` to create a `Post` object from the JSON returned by the server.

#### Parameters

  - decoder: - decoder: The decoder to use for translating the server response to a Swift object.

#### Throws

Error thrown by the `try` attempt when decoding any given property.

## Properties

### `postId`

``` swift
var postId: String?
```

### `slug`

``` swift
var slug: String?
```

### `appearance`

``` swift
var appearance: String?
```

### `language`

``` swift
var language: String?
```

### `rtl`

``` swift
var rtl: Bool?
```

### `createdDate`

``` swift
var createdDate: Date?
```

### `updatedDate`

``` swift
var updatedDate: Date?
```

### `title`

``` swift
var title: String?
```

### `body`

``` swift
var body: String
```

### `tags`

``` swift
var tags: [String]?
```

### `views`

``` swift
var views: Int?
```

### `collectionAlias`

``` swift
var collectionAlias: String?
```
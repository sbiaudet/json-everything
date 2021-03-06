# [1.5.1](https://github.com/gregsdennis/json-everything/pull/34)

[#35](https://github.com/gregsdennis/json-everything/issues/35) `JsonSchema.FromFile()` handles file paths as URIs incorrectly in non-Windows systems. 

# [1.5.0](https://github.com/gregsdennis/json-everything/pull/34)

[#33](https://github.com/gregsdennis/json-everything/issues/33) Added `ValidationOptions.ValidateFormat` which allows configuration of whether to validate the `format` keyword.  Also fixes a bug where the `format` keyword was validated by default for draft 2019-09 which specifies that it should only generate annotations by default.  Because this library favors the latest draft, this is the default behavior for all drafts.

As a further followup to #27 (below), basic output has been refined.

# [1.4.0](https://github.com/gregsdennis/json-everything/pull/31)

[#27](https://github.com/gregsdennis/json-everything/issues/27) (reopened) Better reduction of detailed output format which eliminates the notion that any nodes *must* be kept.

[#29](https://github.com/gregsdennis/json-everything/issues/29) Relative `$id` keyword at root of schema was not supported.  Added `ValidationOptions.DefaultBaseUri` to be used when no other absolute URI is defined by the `$id` keyword.  Also now supports assuming the base URI from the file name.

# [1.3.1](https://github.com/gregsdennis/json-everything/pull/28)

[#27](https://github.com/gregsdennis/json-everything/issues/27) Nodes in the basic and detailed output formats that match the overall outcome should be removed.  This also addresses several other bugs involving the output such as `absoluteKeywordLocation`.

# [1.3.0](https://github.com/gregsdennis/json-everything/pull/25)

[#15](https://github.com/gregsdennis/json-everything/issues/15) Easier navigation of the schema and its subschemas. Added `ISchemaContainer`, `ISchemaCollector`, and `IKeyedSchemaCollector` for the varying sets of subschemas that keywords can have.  Added `SchemaKeywordExtensions.GetSubschemas()` extension method.

[#19](https://github.com/gregsdennis/json-everything/issues/19) Keyword filtering doesn't consider declared draft or `ValidationOptions.ValidateAs`.

# [1.2.0](https://github.com/gregsdennis/json-everything/pull/17)

([json-schema<nsp>.org #358](https://github.com/json-schema-org/json-schema-org.github.io/pull/358)) Published draft 06 meta-schema doesn't match the copy in the spec repo.

[#16](https://github.com/gregsdennis/json-everything/issues/16) `JsonSchema` equality checking.  Along with this, added `IEquatable<T>` to `SchemaKeywordRegistry.Register<T>()`.

[#18](https://github.com/gregsdennis/json-everything/issues/18) `properties` keyword is processed with same priority as `additionalProperties` making keyword order important, but it shouldn't be.

Added `EnumerableExtensions.ContentsEqual()`.

# [1.1.0](https://github.com/gregsdennis/json-everything/pull/11)

Added `SchemaRegistry.Fetch` property to enable automatic downloading of referenced schemas.

# [1.0.3](https://github.com/gregsdennis/json-everything/pull/11)

[#9](https://github.com/gregsdennis/json-everything/pull/11) `if`/`then`/`else` are processed in serialized order instead of processing `if` first.

[#10](https://github.com/gregsdennis/json-everything/pull/10) Bug fix around deserialization of `readonly` keyword.

# [1.0.2](https://github.com/gregsdennis/json-everything/pull/7)

Updated format `json-pointer` to require plain pointers.  URI-encoded pointers are invalid.

# [1.0.1](https://github.com/gregsdennis/json-everything/pull/6)

Updated validation of formats `hostname`, `iri`, `uri`, `regex`, and `time`.

Fixed issue resolving references (`$ref` & `$recursiveRef`) to miscellaneous (non-keyword) schema data.

# 1.0.0

Initial release.
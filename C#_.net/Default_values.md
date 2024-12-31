# Default values of C# types (C# reference)


| Type                                                                                                                                                        | Default value                                                                                                                                                                                                                                                                                                                    |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Any<br />[reference type](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/reference-types)                                         | `null`                                                                                                                                                                                                                                                                                                                         |
| Any<br />[built-in integral numeric type](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types)             | 0 (zero)                                                                                                                                                                                                                                                                                                                         |
| Any<br />[built-in floating-point numeric type](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types) | 0 (zero)                                                                                                                                                                                                                                                                                                                         |
| [bool](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/bool)                                                                  | `false`                                                                                                                                                                                                                                                                                                                        |
| [char](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char)                                                                  | `'\0'` (U+0000)                                                                                                                                                                                                                                                                                                                |
| [enum](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/enum)                                                                  | The value produced by the expression `(E)0`, where `E` is the enum identifier.                                                                                                                                                                                                                                               |
| [struct](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/struct)                                                              | The value produced by setting all value-type fields to their default values and<br />all reference-type fields to `null`.                                                                                                                                                                                                      |
| Any<br />[nullable value type](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types)                          | An instance for which the[HasValue](https://learn.microsoft.com/en-us/dotnet/api/system.nullable-1.hasvalue) property is `false` and the [Value](https://learn.microsoft.com/en-us/dotnet/api/system.nullable-1.value) property is undefined. <br />That default value is also known as the *null* value of a nullable value type. |